---
title: Schützen von Dateien mit DRM Version 7 oder höher
description: Schützen von Dateien mit DRM Version 7 oder höher
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- Windows Medienformat-SDK, Erstellen geschützter Dateien
- Windows Medienformat-SDK, geschützte Dateien
- Advanced Systems Format (ASF), Erstellen geschützter Dateien
- ASF (Advanced Systems Format), Erstellen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF),WMStubDRM.lib
- ASF (Advanced Systems Format), WMStubDRM.lib
- WMStubDRM.lib, Erstellen geschützter Dateien
- WMStubDRM.lib,geschützte Dateien
- Digital Rights Management (DRM), WMStubDRM.lib
- DRM (Digital Rights Management), WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcec136539f9ea5d52fb5c92cf546a965202b35e25bd22010baaf98d8fde7720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846155"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>Schützen von Dateien mit DRM Version 7 oder höher

Um Dateien mit Windows Media DRM Version 7 oder höher zu schützen, verwenden Sie die [**IWMDRMWriter::SetDRMAttribute-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) des Writerobjekts, um DRM-Attribute zu festlegen. Da DRM Version 7 und höher eindeutige Lizenzen für jede geschützte Datei oder jeden Satz von Dateien aktivieren, verfügt **die IWMDRMWriter-Schnittstelle** auch über Methoden zum Erstellen von Schlüsseln. Diese Methoden werden nur zur Vereinfachung bereitgestellt.

Um ASF-Dateien mit DRM Version 7 oder höher zu schützen, führen Sie die folgenden Schritte aus:

1.  Verknüpfen Sie wmstubDRM.lib, und entlinken Sie bei Bedarf die Datei wmvcore.lib.
2.  Rufen Sie die [**WMCreateWriter-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) auf, um den DRM-Writer zu erstellen. Das erste Argument ist reserviert und muss auf NULL **festgelegt werden.**
3.  Legen Sie ein Profil fest, das vom Writer verwendet werden soll, indem [**Sie IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) oder [**IWMWriter::SetProfileByID aufrufen.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) Sie müssen ein Profil im Writer festlegen, bevor Sie DRM-Attribute festlegen. DRM wird nur für Profile unterstützt, die die Windows Media Audio- oder Windows Media Video-Codecs verwenden.
4.  Abrufen der [**IWMDRMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) des Writerobjekts.
5.  Rufen [**Sie IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) auf, und legen Sie [**Advanced \_ \_ DRM verwenden auf**](use-advanced-drm.md) TRUE **fest.**
6.  Wenn Sie einen neuen Schlüsselseed generieren müssen, rufen Sie [**IWMDRMWriter::GenerateKeySeed auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) In den meisten Fällen wird ein zuvor generierter Schlüsselwert wiederverwendt. Dieser Wert muss geheim bleiben. es wird nicht in die Datei geschrieben.
7.  Rufen [**Sie IWMDRMWriter::GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) auf, um eine Schlüssel-ID zu erstellen. Dies ist der zweite Wert, der zum Erstellen des tatsächlichen Schlüssels verwendet wird. Im Gegensatz zum Schlüssel-Seeding ist die Schlüssel-ID öffentlich und wird im DRM-Header klar in die Datei geschrieben. Erstellen Sie eine neue Schlüssel-ID für jede neue Datei, die Sie erstellen.
8.  Rufen **Sie bei Bedarf IWMDRMWriter::GenerateSigningKeyPair** auf, um einen öffentlichen und privaten Schlüssel zu generieren, der zum Signieren des erweiterten DRM ASF-Headerobjekts verwendet wird. Weitere Informationen zu diesen Schlüsseln finden Sie unter [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).
9.  Beziehen Sie bei Bedarf die Werte, um das digitale Signaturobjekt des DRM-Headers zu füllen. Wenn Auf Ihrem System keine funktionierende Version von Windows Media Rights Manager installiert ist, müssen Sie das digitale Signaturobjekt des ASF-Dateiheaders konfigurieren, indem Sie die folgenden vier Attribute angeben, die alle von Microsoft erhalten werden müssen:

    -   [**DRM \_ LASignatureRootCert**](drm-lasignaturerootcert.md)
    -   [**DRM \_ LASignatureCert**](drm-lasignaturecert.md)
    -   [**DRM \_ LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md)
    -   [**DRM \_ LASignaturePrivKey**](drm-lasignatureprivkey.md)

    Wenn Sie Media Rights Manager Windows haben, müssen diese Attribute nicht in Ihrer Anwendung festgelegt werden. Die DRM-Komponente ruft diese Attribute ab und verwendet sie, um den Header automatisch zu signieren. Wenn Sie eine aktivierte Version von Windows Media Rights Manager auf einem anderen Computer haben und diese Digitalen Signaturobjektwerte wiederverwenden möchten, finden Sie sie in der Registrierung. Das Lizenzserverzertifikat wird unter HKEY LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server Certs:cert1 gespeichert, und das Stammzertifikat wird unter \_ \_ \\ \\ \\ \\ \\ HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server \_ \\ \\ \\ \\ \\ Certs:cert2 gespeichert. Wenn Sie Dateien mit DRM Version 7 schützen, müssen Sie die Werte aus diesen Registrierungsschlüsseln verwenden. Verwenden Sie für die **DRM \_ LASignaturePrivKey-Eigenschaft** **entweder GenerateSigningKeysEx** (über das Windows Media Rights Manager SDK), oder verwenden Sie den von Windows Media Rights Manager installierten Wert unter HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License \_ \\ \\ \\ \\ Server:Info \_ Cert0 erneut. Verwenden Sie für die **DRM \_ LASignatureCert-Eigenschaft** entweder **GenerateSigningKeysEx** (über das Windows Media Rights Manager SDK) oder den wert, der von Windows Media Rights Manager unter HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server \_ \\ \\ \\ \\ \\ Certs:cert0 installiert wird.

10. Rufen [**Sie IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) so oft wie erforderlich auf, um das Writer-Objekt zu konfigurieren, wodurch die erforderlichen DRM-Headerattribute nach Bedarf festgelegt werden. Diese Eigenschaften bleiben für die Lebensdauer des Writerobjekts oder so lange erhalten, bis sie mit einem neuen Wert zurückgesetzt werden. Sie müssen nicht für jede neue Datei zurückgesetzt werden, die Sie erstellen.

    Die folgenden Eigenschaften sind für das Writer-Objekt erforderlich:

    -   [**DRM \_ HeaderSignPrivKey**](drm-headersignprivkey.md)
    -   [**DRM \_ KeySeed**](drm-keyseed.md)
    -   [**DRM \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)
    -   [**\_DRM-Schlüssel-ID**](drm-keyid.md)
    -   [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md)

    Die folgenden Eigenschaften sind optional:

    -   [**DRM \_ ContentID**](drm-contentid.md)
    -   [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md)

    Darüber hinaus können Sie benutzerdefinierte DRM-Dateiattribute direkt mithilfe des [**DRM \_ DRMHeader-Basisattributs**](drm-drmheader.md) angeben. Sie können ein beliebiges zusätzliches Attribut hinzufügen, z. B. "DRMHeader.RequireSAP", um zusätzliche Informationen zu kommunizieren, die vom Lizenzserver beim Erstellen der Lizenz verwendet werden. Der Lizenzserver muss im Voraus über zusätzliche Eigenschaften informiert werden, die Sie hinzufügen. Es gibt keine Möglichkeit, unbekannte Eigenschaften programmgesteuert zu finden.

11. Schreiben Sie die Datei [**mithilfe der METHODEN der IWMWriter-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) wie an anderer Stelle in dieser Dokumentation beschrieben. Um einen Live-DRM-Stream zu erstellen, schreiben Sie einfach in eine Netzwerksenke. Sie können auch in eine Pushsenke schreiben.
12. Erstellen Sie bei Bedarf eine Lizenz für die Datei mithilfe Windows Media Rights Manager. Diese Aufgabe kann auch von einem Lizenzserver eines Drittanbieters ausgeführt werden. Bei Live-DRM-Szenarien müssen Endbenutzer eine Lizenz erwerben, bevor der Stream beginnt, oder wenn sie zum ersten Mal versuchen, eine Verbindung damit herzustellen.

**Hinweis:** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**DRM-Attributliste**](drm-attribute-list.md)
</dt> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> <dt>

[**IWMDRMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> <dt>

[**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**IWMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Lesen geschützter Dateien**](reading-protected-files.md)
</dt> <dt>

[**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




