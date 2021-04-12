---
title: Einrichten des Servers für Uploads
description: Zum Hochladen von Dateien auf einen Server mit Bits muss auf dem Server IIS und die BITS-Server Erweiterung ISAPI installiert sein. Informationen zu IIS-Anforderungen finden Sie unter IIS-Anforderungen für BITS-Uploads.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206299"
---
# <a name="setting-up-the-server-for-uploads"></a>Einrichten des Servers für Uploads

Zum Hochladen von Dateien auf einen Server mit Bits muss auf dem Server IIS und die BITS-Server Erweiterung ISAPI installiert sein. Informationen zu IIS-Anforderungen finden Sie unter [IIS-Anforderungen für BITS-Uploads](iis-requirements-for-bits-uploads.md).

Informationen zum Konfigurieren des virtuellen IIS-Verzeichnisses, das Bits für Uploads verwendet, finden Sie in den folgenden Themen.

-   [Festlegen von Berechtigungen für virtuelle Verzeichnisse](setting-permissions-on-virtual-directories.md)
-   [Schreiben eines Skripts zum Konfigurieren des virtuellen Verzeichnisses](writing-a-script-to-configure-the-virtual-directory.md)
-   [Verwenden der IIS-Benutzeroberfläche zum Konfigurieren des virtuellen Verzeichnisses](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Verhindern mehrerer Uploads](preventing-multiple-uploads.md)
-   [Bewährte Methoden für den Upload](upload-best-practices.md)

> [!Note]  
> Einige IIS-Installationen enthalten die URLScan-Filter Komponente. Wenn URLScan aktiviert ist, muss der Administrator das Verb "Bits \_ Post"-Verb in der Liste der zulässigen HTTP-Verben von URLScan hinzufügen. Andernfalls können Bits-Client Uploads nicht ausgeführt werden. Weitere Informationen zum Aktivieren von Verben in URLScan finden Sie in der URLScan-Dokumentation.

 

 

 




