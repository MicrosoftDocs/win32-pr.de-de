---
description: Installiert ein registriertes Zertifikat aus einer PFX-Datei (Personal Information Exchange) im Zertifikat Speicher.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: InstallResponse-frompfx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960463"
---
# <a name="installresponsefrompfx"></a>InstallResponse-frompfx

Mit dem Beispiel "installresponstifrompfx" wird ein registriertes Zertifikat aus einer PFX-Datei (Personal Information Exchange) in den Zertifikat Speicher installiert.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ installresponsefrompfx installiert.

## <a name="discussion"></a>Diskussion

Das InstallResponse-frompfx-Beispiel:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte Folgendes enthalten:
    -   Der Name des Beispiels.
    -   Der Name der PFX-Datei, die das registrierte Zertifikat enthält.
    -   Ein Kennwort, das der PFX-Datei zugeordnet ist.
2.  Liest die PFX-Datei, versucht zunächst das Base64-Format und das Binärformat, wenn Base64 fehlschlägt. Die decodefilew ()-Funktion wird in der Datei "registricommon. cpp" definiert.
3.  Konvertiert das registrierte Zertifikat in ein **BSTR** und verwendet es, um ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt zu initialisieren. Die convertwszdebstr-Funktion ist in der Datei "registricommon. cpp" definiert.
4.  Installiert das Zertifikat im Zertifikat Speicher.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschreibung von "Einschreibung"](enrolleobocmc.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



