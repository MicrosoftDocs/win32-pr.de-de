---
description: Der Pipeserver gibt den Pipetypmodus, den Lesemodus und den Wartemodus im dwPipeMode-Parameter der CreateNamedPipe-Funktion an. Pipeclients können diese Pipemodi für ihre Pipehandles mithilfe der CreateFile-Funktion angeben.
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: Named Pipe-Typ, Lese- und Wartemodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b8ba69ef0d795747070072511c84abf5a3950db3b9c03ec18973f4d29bbd51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014890"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>Named Pipe-Typ, Lese- und Wartemodi

Der Pipeserver gibt den Pipetypmodus, den Lesemodus und den Wartemodus im *dwPipeMode-Parameter* der [**CreateNamedPipe-Funktion**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) an. Pipeclients können diese Pipemodi für ihre Pipehandles mithilfe der [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) angeben.

## <a name="type-mode"></a>Typmodus

Der Typmodus einer Pipe bestimmt, wie Daten in eine Named Pipe geschrieben werden. Daten können über eine Named Pipe entweder als Bytestream oder als Nachrichtenstream übertragen werden. Der Pipeserver gibt den Pipetyp beim Aufrufen von [**CreateNamedPipe an,**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) um eine Instanz einer Named Pipe zu erstellen. Die Typmodi müssen für alle Instanzen einer Pipe identisch sein.

Um eine Pipe vom Typ Byte zu erstellen, geben Sie PIPE \_ TYPE \_ BYTE an, oder verwenden Sie den Standardwert. Die Daten werden als Bytestream in die Pipe geschrieben, und das System unterscheidet nicht zwischen den Bytes, die in verschiedenen Schreibvorgängen geschrieben wurden.

Um eine Pipe vom Typ message zu erstellen, geben Sie PIPE \_ TYPE \_ MESSAGE an. Das System behandelt die Bytes, die bei jedem Schreibvorgang in die Pipe geschrieben werden, als Nachrichteneinheit. Das System führt Schreibvorgänge für Nachrichtentyppipes immer so aus, als wäre der Schreibmodus aktiviert.

## <a name="read-mode"></a>Lesemodus

Der Lesemodus einer Pipe bestimmt, wie Daten aus einer Named Pipe gelesen werden. Der Pipeserver gibt den anfänglichen Lesemodus für ein Pipehandle beim Aufrufen [**von CreateNamedPipe an.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) Daten können im Bytelesemodus oder im Nachrichtenlesemodus gelesen werden. Ein Handle für eine Bytetyppipe kann sich nur im Bytelesemodus befinden. Ein Handle für eine Nachrichtentyppipe kann sich entweder im Byte- oder Nachrichtenlesemodus befinden. Bei einer Nachrichtentyppipe kann der Lesemodus für Server- und Clienthandles zur gleichen Pipeinstanz unterschiedlich sein.

Um das Pipehandles im Bytelesemodus zu erstellen, geben Sie PIPE \_ READMODE \_ BYTE an, oder verwenden Sie den Standardwert. Daten werden aus der Pipe als Bytestream gelesen. Ein Lesevorgang wird erfolgreich abgeschlossen, wenn alle verfügbaren Bytes in der Pipe gelesen werden oder wenn die angegebene Anzahl von Bytes gelesen wird.

Um das Pipehandles im Nachrichtenlesemodus zu erstellen, geben Sie PIPE \_ READMODE \_ MESSAGE an. Daten werden aus der Pipe als Nachrichtenstream gelesen. Ein Lesevorgang wird nur erfolgreich abgeschlossen, wenn die gesamte Nachricht gelesen wird. Wenn die angegebene Anzahl zu lesenden Bytes kleiner als die Größe der nächsten Nachricht ist, liest die Funktion so viel wie möglich die Nachricht, bevor sie 0 (null) zurückgibt (die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ MORE DATA \_ zurück). Der Rest der Nachricht kann mit einem anderen Lesevorgang gelesen werden.

Bei einem Pipeclient befindet sich ein von [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zurückgegebenes Pipehandles anfänglich immer im Bytelesemodus. Sowohl Pipeclients als auch Pipeserver können die [**Funktion SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) verwenden, um den Lesemodus eines Pipehandles zu ändern. Das Pipehand handle muss über das Zugriffsrecht FILE \_ WRITE \_ ATTRIBUTES verfügen.

## <a name="wait-mode"></a>Wartemodus

Der Wartemodus eines Pipehandles bestimmt, wie die [**Funktionen ReadFile,**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)und [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) lange Vorgänge verarbeiten. Im Blockierungswartemodus warten die Funktionen unbegrenzt, bis ein Prozess am anderen Ende der Pipe einen Vorgang abgeschlossen hat. Im Nichtblockierungs-Wartemodus geben die Funktionen sofort in Situationen zurück, die andernfalls eine unbegrenzte Wartezeit erfordern würden.

Ein [**ReadFile-Vorgang**](/windows/desktop/api/fileapi/nf-fileapi-readfile) wird vom Wartemodus eines Pipehandles beeinflusst, wenn die Pipe leer ist. Bei einem Blockierungs-Wait-Handle wird der Vorgang erst erfolgreich abgeschlossen, wenn Daten von einem Thread verfügbar sind, der an das andere Ende der Pipe schreibt. Bei Verwendung eines nicht blockierenden Wait-Handles gibt die Funktion sofort 0 (null) zurück, und die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ NO DATA \_ zurück.

Ein [**WriteFile-Vorgang**](/windows/desktop/api/fileapi/nf-fileapi-writefile) wird durch den Wartemodus eines Pipehandpunkts beeinflusst, wenn nicht genügend Speicherplatz im Puffer der Pipe verfügbar ist. Bei einem Blockierungswartehandles kann der Schreibvorgang erst erfolgreich ausgeführt werden, wenn durch einen Thread, der vom anderen Ende der Pipe liest, genügend Speicherplatz im Puffer erstellt wird. Bei einem Nichtblockierungs-Wait-Handle gibt der Schreibvorgang sofort einen Wert ungleich 0 (null) zurück, ohne Bytes (für eine Pipe vom Nachrichtentyp) oder nach dem Schreiben so viele Bytes wie der Puffer enthält (für eine Pipe vom Typ Byte).

Ein [**ConnectNamedPipe-Vorgang**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) wird vom Wartemodus eines Pipehandles beeinflusst, wenn kein Client verbunden ist oder darauf wartet, eine Verbindung mit der Pipeinstanz herzustellen. Bei einem Blockierungswartehandle ist der Verbindungsvorgang erst erfolgreich, wenn ein Pipeclient eine Verbindung mit der Pipeinstanz herstellt, indem entweder die [**CreateFile-**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) oder [**CallNamedPipe-Funktion aufruft.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) Bei einem Nichtblockierungs-Wait-Handle gibt der Verbindungsvorgang sofort 0 (null) zurück, und die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ PIPE \_ LISTENING zurück.

Standardmäßig werden alle named pipe-Handles, die von [**der CreateNamedPipe-**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) oder [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zurückgegeben werden, mit aktivierter Blockierungswartemodus erstellt. Um die Pipe im Nichtblockierungs-Wartemodus zu erstellen, gibt der Pipeserver PIPE \_ NOWAIT beim Aufrufen von **CreateNamedPipe an.**

Sowohl Pipeclients als auch Pipeserver können den Wartemodus eines Pipehandles ändern, indem sie entweder PIPE WAIT oder PIPE NOWAIT in einem Aufruf der \_ \_ [**SetNamedPipeHandleState-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) angeben.

> [!Note]  
> Der Nichtblockierungs-Wartemodus wird aus Kompatibilitätsgestützt mit Microsoft LAN Manager Version 2.0 unterstützt. Dieser Modus sollte nicht verwendet werden, um überlappende Eingaben und Ausgaben (E/A) mit Named Pipes zu erzielen. Stattdessen sollten überlappende E/A-Vorgänge verwendet werden, da dadurch zeitaufwändige Vorgänge im Hintergrund ausgeführt werden können, nachdem die Funktion zurückgegeben wurde. Weitere Informationen zu überlappenden E/A-Ausgaben finden Sie unter Synchrone und [überlappende Eingabe und Ausgabe.](synchronous-and-overlapped-input-and-output.md)

 

 

 
