---
description: Weitere Informationen finden Sie in der verwalteten Referenz zu Extensible Storage Engine.
title: Verwaltete Referenz zu Extensible Storage Engine
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041916"
---
# <a name="extensible-storage-engine-managed-reference"></a>Verwaltete Referenz zu Extensible Storage Engine

Suchen Sie nach Referenzinformationen für die managedesent-Bibliothek. Die managedesent-Bibliothek bietet verwalteten Zugriff auf ESENT, das einbettbare Datenbankmodul, das in Windows System eigen ist.


_**Gilt für:** Windows | Windows Server_

**Inhalt dieses Artikels:**  
Wie unterscheidet sich die managedesent-Bibliothek von ESENT?  
Anforderungen  
In diesem Abschnitt  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>Wie unterscheidet sich die managedesent-Bibliothek von ESENT?

ESENT ist eine einbettbare, transaktionale Datenbank-Engine, mit der Sie benutzerdefinierte Anwendungen erstellen können, die eine zuverlässige, hochleistungsfähige Speicherung von Daten benötigen. Die ESENT-Engine kann bei Datenanforderungen helfen, die von etwas einfachem wie einer zu großen Hash Tabelle, die zu groß für die Speicherung im Arbeitsspeicher ist, bis hin zu komplexen Daten, wie z. b. einer Anwendung mit Tabellen, Spalten und Indizes, reichen. Um eine Anwendung mit ESENT zu erstellen, verwenden Sie die esent.dll-dll, die Teil des Windows-Betriebssystems ist, und schreiben Ihren Code mit C/C++. Weitere Informationen zu ESENT finden Sie unter [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).

Managedesent baut auf esent.dll auf, die Teil von Windows ist, sodass keine zusätzlichen nicht verwalteten Binärdateien zum herunterladen und installieren vorhanden sind. Mit der managedesent-Bibliothek können Sie die Anwendung erstellen, indem Sie eine verwaltete Sprache, wie z. b. c, \# anstelle von c/C++ verwenden. Die Bibliothek verwendet die gleichen Typen-und Elementnamen, um die ESE-API verfügbar zu machen. Wenn Sie also bereits mit der Struktur dieser API vertraut sind, können Sie problemlos zu dieser verwalteten Bibliothek wechseln.

## <a name="requirements"></a>Anforderungen

Für diese verwaltete Bibliothek ist Folgendes erforderlich:

  - Ein Computer, auf dem eine Windows-Version ab Windows Vista ausgeführt wird

  - Visual Studio 2012

  - Das .NET Framework 4.5

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
