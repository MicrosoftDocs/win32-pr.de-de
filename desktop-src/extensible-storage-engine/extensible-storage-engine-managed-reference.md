---
description: Weitere Informationen finden Sie unter Extensible Storage Engine Managed Reference
title: Erweiterbare Storage-Engine – Verwaltete Referenz
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: 38f7f09d441fa6f4158594caa8eda0b15bbe07fe909a73cd194f0886bb29914d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093680"
---
# <a name="extensible-storage-engine-managed-reference"></a>Erweiterbare Storage-Engine – Verwaltete Referenz

Hier finden Sie Referenzinformationen für die ManagedESENT-Bibliothek. Die ManagedESENT-Bibliothek bietet verwalteten Zugriff auf ESENT, die einbettbare Datenbank-Engine, die nativ Windows.


_**Gilt für:** Windows | Windows Server_

**Inhalt dieses Artikels:**  
Wie ist die ManagedESENT-Bibliothek anders als ESENT?  
Anforderungen  
In diesem Abschnitt  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>Wie ist die ManagedESENT-Bibliothek anders als ESENT?

ESENT ist eine einbettbare, transaktionale Datenbank-Engine, mit der Sie benutzerdefinierte Anwendungen erstellen können, die eine zuverlässige, hochleistungsfähige Speicherung von Daten mit geringem Mehraufwand benötigen. Die ESENT-Engine kann bei Datenanforderungen helfen, die von einer einfachen Hashtabelle, die zu groß für die Speicherung im Arbeitsspeicher ist, bis hin zu komplexeren Daten, z. B. einer Anwendung mit Tabellen, Spalten und Indizes, reichen. Um eine Anwendung mit ESENT zu erstellen, verwenden Sie die esent.dll-DLL, die Teil des Windows-Betriebssystems ist, und schreiben Ihren Code mit C/C++. Weitere Informationen zu ESENT finden Sie unter Extensible Storage Engine Reference (Referenz zur [erweiterbaren Storage-Engine).](./extensible-storage-engine-reference.md)

ManagedESENT basiert auf esent.dll, die Teil von Windows ist, sodass es keine zusätzlichen nicht verwalteten Binärdateien zum Herunterladen und Installieren gibt. Mit der ManagedESENT-Bibliothek können Sie Ihre Anwendung mithilfe einer verwalteten Sprache wie C anstelle von \# C/C++ erstellen. Die Bibliothek verwendet dieselben Typ- und Membernamen, um die ESE-API verfügbar zu machen. Wenn Sie also bereits mit der Struktur dieser API vertraut sind, können Sie problemlos zu dieser verwalteten Bibliothek überwechseln.

## <a name="requirements"></a>Anforderungen

Diese verwaltete Bibliothek erfordert Folgendes:

  - Ein Computer, auf dem eine Version von Windows ab Windows Vista ausgeführt wird

  - Visual Studio 2012

  - Das .NET Framework 4.5

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)

  - [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
