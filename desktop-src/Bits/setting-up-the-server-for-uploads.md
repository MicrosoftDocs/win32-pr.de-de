---
title: Einrichten des Servers für Uploads
description: Zum Hochladen von Dateien auf einen Server mit BITS müssen IIS und die BITS-Servererweiterung ISAPI auf dem Server installiert sein. IiS-Anforderungen finden Sie unter IIS-Anforderungen für BITS-Uploads.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e075478f6e0335c6bf601a9289d93d4d3fac2aefd9e4f1ef820e938a1bfc0ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004720"
---
# <a name="setting-up-the-server-for-uploads"></a>Einrichten des Servers für Uploads

Zum Hochladen von Dateien auf einen Server mit BITS müssen IIS und die BITS-Servererweiterung ISAPI auf dem Server installiert sein. Informationen zu IIS-Anforderungen finden Sie unter [IIS-Anforderungen für BITS-Uploads.](iis-requirements-for-bits-uploads.md)

Informationen zum Konfigurieren des virtuellen IIS-Verzeichnisses, das BITS für Uploads verwendet, finden Sie in den folgenden Themen.

-   [Festlegen von Berechtigungen für virtuelle Verzeichnisse](setting-permissions-on-virtual-directories.md)
-   [Schreiben eines Skripts zum Konfigurieren des virtuellen Verzeichnisses](writing-a-script-to-configure-the-virtual-directory.md)
-   [Verwenden der IIS-Benutzeroberfläche zum Konfigurieren des virtuellen Verzeichnisses](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Verhindern mehrerer Uploads](preventing-multiple-uploads.md)
-   [Hochladen Bewährte Methoden](upload-best-practices.md)

> [!Note]  
> Einige IIS-Installationen enthalten die UrlScan-Filterkomponente. Wenn UrlScan aktiviert ist, muss der Administrator das VERB "BITS \_ POST" der Liste der zulässigen HTTP-Verben von UrlScan hinzufügen. Andernfalls schlagen BITS-Clientuploads fehl. Weitere Informationen zum Aktivieren von Verben in UrlScan finden Sie in der UrlScan-Dokumentation.

 

 

 




