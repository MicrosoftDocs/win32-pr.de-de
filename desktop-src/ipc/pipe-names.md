---
description: Jeder Named Pipe hat einen eindeutigen Namen, der ihn von anderen benannten Pipes in der System Liste benannter Objekte unterscheidet. Ein pipenserver gibt einen Namen für die Pipe an, wenn die Funktion "" die Funktion "" erstellt, um eine oder mehrere Instanzen einer Named Pipe zu erstellen.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Pipenamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352286"
---
# <a name="pipe-names"></a>Pipenamen

Jede Named Pipe hat einen eindeutigen Namen, der Sie von anderen benannten Pipes in der Liste benannter Objekte des Systems unterscheidet. Ein pipenserver gibt einen Namen für die Pipe an, wenn [**die Funktion "**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) " die Funktion "" erstellt, um eine oder mehrere Instanzen einer Named Pipe zu erstellen. Pipe-Clients geben den Pipenamen an, wenn Sie die Funktion "up [**" oder "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) " aufrufen, um eine Verbindung mit einer Instanz des Named Pipe herzustellen.

Verwenden Sie das folgende Formular, wenn Sie den Namen einer Pipe in der Funktion "up- [**File**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)", " [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)" oder " [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) " angeben:

\\\\*Servername* \\ \\*Pipename* der Pipe

Dabei ist *Server* Name entweder der Name eines Remote Computers oder ein Zeitraum, um den lokalen Computer anzugeben. Die von *Pipename* angegebene Pipe-namens Zeichenfolge kann ein beliebiges Zeichen enthalten, das kein umgekehrter Schrägstrich ist, einschließlich Zahlen und Sonderzeichen. Die Zeichenfolge für den gesamten Pipenamen kann bis zu 256 Zeichen lang sein. Bei Pipenamen wird die Groß-/Kleinschreibung nicht beachtet

Der Pipeserver kann eine Pipe nicht auf einem anderen Computer erstellen, daher muss " [**anatenamedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) " einen Punkt für den Servernamen verwenden, wie im folgenden Beispiel gezeigt.

\\\\.\\ \\*Pipename* der Pipe

Ein Pipeserver kann den Pipenamen an die Pipe-Clients bereitstellen, sodass er eine Verbindung mit der Pipe herstellen kann. Der Pipeclient ermittelt den Pipenamen aus einer permanenten Quelle, z. b. einem Registrierungs Eintrag, einer Datei oder einer anderen Anwendung. Andernfalls müssen die Clients den Pipenamen zum Zeitpunkt der Kompilierung kennen.

 

 
