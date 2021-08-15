---
description: Die Imageintegritätsfunktionen verwalten den Satz von Zertifikaten in einer Imagedatei.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Bildintegritätsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a2311ccfc59fb228a8f71c380205dc754452ba4a9d0a7e1dcb3c9edcd92a14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957099"
---
# <a name="image-integrity-functions"></a>Bildintegritätsfunktionen

Die Imageintegritätsfunktionen verwalten den Satz von Zertifikaten in einer Imagedatei. Routinen werden zum Hinzufügen, Entfernen und Abfragen von Zertifikaten bereitgestellt. Es ist auch eine Funktion zum Abrufen des Bytestreams einer Bilddatei verfügbar, die zum Berechnen eines Nachrichtenh digest der Bilddatei erforderlich ist. Dies ist erforderlich, um Signaturzertifikate zu erstellen.

Jedes Zertifikat in einer Datei verfügt über einen Index, der sich ändern kann, wenn Zertifikate entfernt werden. Neue Zertifikate werden immer "am Ende" der Liste der vorhandenen Zertifikate hinzugefügt. Das heißt, ihnen werden Indizes zugewiesen, die größer sind als alle derzeit in Gebrauchenen Indizes. Im Allgemeinen sollte eine Anwendung nicht davon ausgehen, dass ein bestimmtes Zertifikat über denselben Index verfügt, den sie beim letzten Verweis auf das Zertifikat hatte.

-   [**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



