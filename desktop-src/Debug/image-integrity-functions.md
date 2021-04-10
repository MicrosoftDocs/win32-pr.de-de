---
description: Die Bild Integritäts Funktionen verwalten den Satz von Zertifikaten in einer Bilddatei.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Bild Integritäts Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041410"
---
# <a name="image-integrity-functions"></a>Bild Integritäts Funktionen

Die Bild Integritäts Funktionen verwalten den Satz von Zertifikaten in einer Bilddatei. Routinen werden bereitgestellt, um Zertifikate hinzuzufügen, zu entfernen und abzufragen. Es ist auch eine Funktion zum Abrufen des Bytestreams einer Bilddatei verfügbar, die zum Berechnen eines Nachrichten Digest der Bilddatei erforderlich ist. Dies ist zum Erstellen von Signatur Zertifikaten erforderlich.

Jedes Zertifikat in einer Datei verfügt über einen Index, der sich ändern kann, wenn Zertifikate entfernt werden. Neue Zertifikate werden immer am Ende der Liste vorhandener Zertifikate hinzugefügt. Das heißt, es werden Indizes zugewiesen, die größer sind als alle derzeit verwendeten Indizes. Im Allgemeinen sollte eine Anwendung nicht davon ausgehen, dass ein bestimmtes Zertifikat denselben Index wie das letzte Mal referenziert hat.

-   [**Digestfunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [**Imageaddcertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [**Imageenumeratecertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [**Imagegetcertificatedata**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [**Imagegetcertifialisieheader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [**Imagegetdigeststream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [**Imageremovecertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



