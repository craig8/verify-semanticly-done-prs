FROM python:3.10

# Install Poetry
RUN curl -sSL https://install.python-poetry.org | POETRY_VERSION=2.0.0 python3 - && \
    mv $HOME/.local/bin/poetry /usr/local/bin/poetry

# Set the working directory
WORKDIR /workspace

# Copy the project files into the container
COPY . /workspace

# Install project dependencies
RUN poetry install

# Set the default command to bash
CMD ["bash"]
