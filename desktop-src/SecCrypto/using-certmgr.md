---
description: Verwenden Sie certmgr, um Zertifikate, CRLs und CTLs aus einer Datei oder einem Zertifikat Speicher anzuzeigen, Zertifikate in einen Zertifikat Speicher zu kopieren, Zertifikate aus einem Zertifikat Speicher zu löschen und Zertifikate in Dateien zu speichern.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Verwenden von certmgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347250"
---
# <a name="using-certmgr"></a>Verwenden von certmgr

[Certmgr](certmgr.md) kann verwendet werden, um [*Zertifikate*](../secgloss/c-gly.md), [*Zertifikats Sperr Listen*](../secgloss/c-gly.md) (CRLs) und [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs) aus einer Datei oder einem Zertifikat Speicher anzuzeigen, Zertifikate in einen [*Zertifikat Speicher*](../secgloss/c-gly.md)zu kopieren, Zertifikate aus einem Zertifikat Speicher zu löschen und Zertifikate in Dateien zu speichern.

Wenn [Certmgr](certmgr.md) ohne Optionen verwendet wird, wird ein certmgr-Assistent angezeigt, der den Benutzer durch den Vorgang führt.

Bei der Datei muss es sich um einen der folgenden Typen handeln:

-   Eine codierte CTL-, CRL-oder Zertifikatsdatei (kann Base-64-codiert sein)
-   Eine PKCS \# 7-Datei
-   Eine SPC-Datei
-   Ein signiertes Dokument
-   Eine serialisierte StoreFile

In den folgenden Beispielen werden die Befehle " [Certmgr](certmgr.md) " verwendet, um allgemeine Zertifikat Aufgaben auszuführen.

-   Zeigen Sie die Zertifikate, CRLs und CTLs aus " *MyFile. ext*" an.

    **Certmgr** *MyFile. ext*

-   Zeigen Sie die Zertifikate, CRLs und CTLs aus dem eigenen Systemspeicher an.

    **certmgr-s My**

-   Kopieren Sie alle Zertifikate, CRLs und CTLs in eine Datei mit dem Namen " *MyFile. ext* " in eine neue Datei mit dem Namen " *NewFile. ext*".

    **Certmgr-Add-All-c** *MyFile. ext* *NewFile. ext*

-   Kopieren Sie alle Zertifikate, CRLs und CTLs aus dem eigenen Systemspeicher in eine Datei mit dem Namen *newmyfile. ext*.

    **Certmgr-Add-All-c-s My** *newmyfile. ext*

-   Kopieren Sie ein Zertifikat mit dem allgemeinen Namen *MyCert* im eigenen Systemspeicher in eine Datei mit dem Namen *newCert. CER*.

    **Certmgr-Add-c-n** *MyCert* **-s My** *newCert. CER*

-   Löschen Sie alle Zertifikate aus dem eigenen Systemspeicher.

    **certmgr-del-all-c-s My**

-   Löschen Sie alle CTLs aus dem eigenen Systemspeicher, und speichern Sie den resultierenden Speicher in einer Datei mit dem Namen *newStore. Str*.

    **certmgr-del-all-CTL-s My** *newStore. Str*

-   Speichern Sie in einer Datei mit dem Namen *newCert. CER*, einem Zertifikat, bei dem es sich um ein [*X. 509*](../secgloss/x-gly.md) -codiertes Zertifikat mit dem allgemeinen Namen *MyCert* handelt, das sich im Stamm Zertifikat Speicher befindet.

    **Certmgr-Put-c-n** *MyCert* **-s root** *newCert. CER*

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertMgr](certmgr.md)
</dt> </dl>

 

 
