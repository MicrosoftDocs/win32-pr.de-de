---
title: Asynchrone Verbund Dateien
description: Asynchrone Verbund Dateien, die vom System bereitgestellte Implementierung des asynchronen Speichers, ermöglichen das effiziente herunterladen von Verbund Dateien aus dem Internet im allgemeinen und im Internet.
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04de2162b50283b12bc8deed6ec908d92e7584d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390794"
---
# <a name="asynchronous-compound-files"></a>Asynchrone Verbund Dateien

Asynchrone Verbund Dateien, die vom System bereitgestellte Implementierung des asynchronen Speichers, ermöglichen das effiziente herunterladen von Verbund Dateien aus dem Internet im allgemeinen und im Internet. Die grundlegende Architektur von asynchronen Verbund Dateien ist im folgenden Diagramm dargestellt.

![grundlegende Architektur für asynchrone Verbund Dateien](images/asy-stor.png)

Die asynchrone Implementierung der Verbund Dateien kann mit neuen asynchronen monikertypen funktionieren, die Internet Protokolle verstehen und an ein Objekt gebunden werden können, das durch eine URL identifiziert wird. Ein solcher Moniker würde einen asynchronen [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -oder [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Zeiger aus dem Aufruf von [**IMoniker:: bindesstorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage)des Clients zurückgeben.

Verbund Dateien werden im Allgemeinen auf einem Bytearray-Objekt implementiert, einer Abstraktion einer Datei, die die Daten eines Objekts als flatbytearray darstellt. Das Bytearray-Objekt macht seine Funktionalität über die [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) -Schnittstelle verfügbar. Wenn ein Bytearray eine nicht blockierende asynchrone Speicherung unterstützt, wird E \_ bis zur Implementierung der Verbund Datei zurückgegeben, wodurch der Fehler wiederum an den Aufrufer weitergegeben wird.

Um die während eines Downloads verfügbaren Daten nachzuverfolgen, macht ein Bytearray, das den asynchronen Speicher unterstützt, die [**ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) -Schnittstelle für ein Wrapper Objekt verfügbar, das speziell für diesen Zweck vom System bereitgestellt wird. Der von einem asynchronen Moniker bereitgestellte Downloadcode ruft diese Schnittstelle auf, um das Bytearray asynchron auszufüllen, da Daten verfügbar sind. Das Wrapper Objekt macht auch eine **ILockBytes** -Schnittstelle verfügbar, die die asynchrone Implementierung von Verbund Dateien zum Lesen und Schreiben von Daten aus und in das Array verwendet.

Asynchrone Speicher-und Streamobjekte stellen einen Verbindungspunkt für die [**iprogressnotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) -Schnittstelle bereit, die durch den Downloadcode des asynchronen Monikers implementiert wird. Die Implementierung der asynchronen Verbund Dateien ruft **iprogressnotify** auf, um dem Download Programminformationen zum Status des Downloadvorgangs bereitzustellen.

 

 