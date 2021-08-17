---
description: Installiert ein registriertes Zertifikat aus einer PFX-Datei (Personal Information Exchange) im Zertifikatspeicher.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540e719f098d227afac4af59fd2d296d9d06606d04b9de80cf1e24081918d6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117777606"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

Im Beispiel installResponseFromPFX wird ein registriertes Zertifikat aus einer PFX-Datei (Personal Information Exchange) im Zertifikatspeicher installiert.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ installResponseFromPFX installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Das InstallResponseFromPFX-Beispiel:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte Folgendes enthalten:
    -   Der Name des Beispiels.
    -   Der Name der PFX-Datei, die das registrierte Zertifikat enthält.
    -   Ein Kennwort, das der PFX-Datei zugeordnet ist.
2.  Liest die PFX-Datei und versucht zuerst das Base64-Format und das Binärformat, wenn Base64 fehlschlägt. Die DecodeFileW()-Funktion ist in enrollCommon.cpp definiert.
3.  Konvertiert das registrierte Zertifikat in einen **BSTR** und verwendet es, um ein [**IX509Enrollment-Objekt zu**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) initialisieren. Die convertWszToBstr-Funktion ist in enrollCommon.cpp definiert.
4.  Installiert das Zertifikat im Zertifikatspeicher.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[enrollEOBOCMC](enrolleobocmc.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



