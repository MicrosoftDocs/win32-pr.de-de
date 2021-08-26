---
title: Asynchrone Verbunddateien
description: Asynchrone Verbunddateien, die vom System bereitgestellte Implementierung des asynchronen Speichers, ermöglichen das effiziente Herunterladen von Verbunddateien aus dem Internet im Allgemeinen und aus dem Web im Besonderen.
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15404f33041fb52f5baa5230f69434ce390b985c41374235c1f3979ef6c2f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034985"
---
# <a name="asynchronous-compound-files"></a>Asynchrone Verbunddateien

Asynchrone Verbunddateien, die vom System bereitgestellte Implementierung des asynchronen Speichers, ermöglichen das effiziente Herunterladen von Verbunddateien aus dem Internet im Allgemeinen und aus dem Web im Besonderen. Die grundlegende Architektur von asynchronen Verbunddateien ist im folgenden Diagramm dargestellt.

![Grundlegende Architektur von asynchronen Verbunddateien](images/asy-stor.png)

Die Implementierung von Asynchronen Verbunddateien kann mit neuen asynchronen Monikertypen funktionieren, die Internetprotokolle verstehen und an ein durch eine URL identifiziertes Objekt gebunden werden können. Ein solcher Moniker würde einen asynchronen [**IStream-**](/windows/desktop/api/Objidl/nn-objidl-istream) oder [**IStorage-Zeiger**](/windows/desktop/api/Objidl/nn-objidl-istorage) aus dem Aufruf von [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage)des Clients zurückgeben.

Verbunddateien werden im Allgemeinen auf einem Bytearrayobjekt implementiert, einer Abstraktion einer Datei, die die Daten eines Objekts als flaches Bytearray darstellt. Das Bytearrayobjekt macht seine Funktionalität über die [**ILockBytes-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) verfügbar. Wenn ein Bytearray nicht blockierenden asynchronen Speicher unterstützt, wird E PENDING an die Verbunddateiimplementierung zurückgegeben, die den Fehler wiederum an den \_ Aufrufer zurückgibt.

Zum Nachverfolgen der während eines Downloads verfügbaren Daten macht ein Bytearray, das asynchronen Speicher unterstützt, die [**IFillLockBytes-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) für ein Wrapperobjekt verfügbar, das vom System speziell für diesen Zweck bereitgestellt wird. Der heruntergeladene Code, der von einem asynchronen Moniker bereitgestellt wird, ruft diese Schnittstelle auf, um das Bytearray asynchron zu füllen, da Daten verfügbar sind. Das Wrapperobjekt macht auch eine **ILockBytes-Schnittstelle** verfügbar, die von der Implementierung asynchroner Verbunddateien zum Lesen und Schreiben von Daten aus und in das Array verwendet wird.

Asynchrone Speicher- und Streamobjekte stellen einen Verbindungspunkt für die [**IProgressNotify-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) bereit, die durch den downloadenden Code des asynchronen Monikers implementiert wird. Die Implementierung von Asynchronen Verbunddateien ruft **IProgressNotify** auf, um dem Downloader Informationen zum Status des Downloadvorgang zur Verfügung zu stellen.

 

 