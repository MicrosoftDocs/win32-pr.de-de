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
- ASF (Advanced Systems Format),WMStubDRM.lib
- WMStubDRM.lib,Erstellen geschützter Dateien
- WMStubDRM.lib,geschützte Dateien
- Digital Rights Management (DRM),WMStubDRM.lib
- DRM (Verwaltung digitaler Rechte),WMStubDRM.lib
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

Verwenden Sie zum Schützen von Dateien mit Windows Media DRM Version 7 oder höher die [**IWMDRMWriter::SetDRMAttribute-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) des Writerobjekts, um DRM-Attribute festzulegen. Da DRM Version 7 und höhere Versionen eindeutige Lizenzen für jede geschützte Datei oder jeden Satz von Dateien aktivieren, verfügt die **IWMDRMWriter-Schnittstelle** auch über Methoden zum Erstellen von Schlüsseln. Diese Methoden werden nur zur Vereinfachung bereitgestellt.

Führen Sie zum Schützen von ASF-Dateien mit DRM Version 7 oder höher die folgenden Schritte aus:

1.  Link zu WMStubDRM.lib und ggf. Aufheben der Verknüpfung von wmvcore.lib.
2.  Rufen Sie die [**WMCreateWriter-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) auf, um den DRM-Writer zu erstellen. Das erste Argument ist reserviert und muss auf **NULL** festgelegt werden.
3.  Legen Sie ein Profil für den zu verwendenden Writer fest, indem [**Sie IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) oder [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)aufrufen. Sie müssen ein Profil im Writer festlegen, bevor Sie DRM-Attribute festlegen. DRM wird nur für Profile unterstützt, die die Codecs "Windows Media Audio" oder "Windows Media Video" verwenden.
4.  Rufen Sie die [**IWMDRMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) des Writerobjekts ab.
5.  Rufen Sie [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) auf, und legen [**Sie \_ \_ Erweitertes DRM verwenden**](use-advanced-drm.md) auf **TRUE** fest.
6.  Wenn Sie einen neuen Schlüsselseeding generieren müssen, rufen [**Sie IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed)auf. In den meisten Fällen wird ein zuvor generierter Schlüsselwert wiederverwendet. Dieser Wert muss geheim bleiben. sie wird nicht in die Datei geschrieben.
7.  Rufen Sie [**IWMDRMWriter::GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) auf, um eine Schlüssel-ID zu erstellen. Dies ist der zweite Wert, der zum Erstellen des tatsächlichen Schlüssels verwendet wird. Im Gegensatz zum Ausgangswert des Schlüssels ist die Schlüssel-ID öffentlich und wird im DRM-Header im Klartext in die Datei geschrieben. Erstellen Sie eine neue Schlüssel-ID für jede neue Datei, die Sie erstellen.
8.  Rufen Sie bei Bedarf **IWMDRMWriter::GenerateSigningKeyPair** auf, um einen öffentlichen und privaten Schlüssel zu generieren, der zum Signieren des erweiterten DRM-ASF-Headerobjekts verwendet wird. Weitere Informationen zu diesen Schlüsseln finden Sie unter [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).
9.  Rufen Sie bei Bedarf die Werte ab, um das digitale Signaturobjekt des DRM-Headers aufzufüllen. Wenn auf Ihrem System keine funktionierende Version von Windows Media Rights Manager installiert ist, müssen Sie das digitale Signaturobjekt des ASF-Dateiheaders konfigurieren, indem Sie die folgenden vier Attribute angeben, die alle von Microsoft abgerufen werden müssen:

    -   [**DRM \_ LASignatureRootCert**](drm-lasignaturerootcert.md)
    -   [**DRM \_ LASignatureCert**](drm-lasignaturecert.md)
    -   [**DRM \_ LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md)
    -   [**DRM \_ LASignaturePrivKey**](drm-lasignatureprivkey.md)

    Wenn Sie Windows Media Rights Manager installiert haben, müssen Sie diese Attribute nicht in Ihrer Anwendung festlegen. Die DRM-Komponente ruft diese Attribute ab und verwendet sie, um den Header automatisch zu signieren. Wenn Sie über eine aktivierte Version von Windows Media Rights Manager auf einem anderen Computer verfügen und diese Werte für digitale Signaturobjekte wiederverwenden möchten, finden Sie sie in der Registrierung. Das Lizenzserverzertifikat wird unter HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server \_ \\ \\ \\ \\ \\ Certs:cert1 gespeichert, und das Stammzertifikat wird unter HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server \_ \\ \\ \\ \\ \\ Certs:cert2 gespeichert. Beim Schützen von Dateien mit DRM Version 7 müssen Sie die Werte aus diesen Registrierungsschlüsseln verwenden. Verwenden Sie für die **\_ DRM-Eigenschaft LASignaturePrivKey** entweder **GenerateSigningKeysEx** (über das Windows Media Rights Manager SDK), oder verwenden Sie den von Windows Media Rights Manager installierten Wert unter HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License \_ \\ \\ \\ \\ Server:Info \_ Cert0. Verwenden Sie für die **\_ DRM-Eigenschaft LASignatureCert** entweder **GenerateSigningKeysEx** (über das Windows Media Rights Manager SDK) oder den von Windows Media Rights Manager installierten Wert unter HKEY \_ LOCAL MACHINE SOFTWARE Microsoft WM Rights Manager License Server \_ \\ \\ \\ \\ \\ Certs:cert0.

10. Rufen Sie [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) so oft wie nötig auf, um das Writer-Objekt zu konfigurieren, wodurch die erforderlichen DRM-Headerattribute nach Bedarf festgelegt werden. Diese Eigenschaften bleiben für die Lebensdauer des Writerobjekts oder bis sie mit einem neuen Wert zurückgesetzt werden. Sie müssen nicht für jede neu erstellte Datei zurückgesetzt werden.

    Die folgenden Eigenschaften sind für das Writer-Objekt erforderlich:

    -   [**\_DRM-HeaderSignPrivKey**](drm-headersignprivkey.md)
    -   [**DRM \_ KeySeed**](drm-keyseed.md)
    -   [**DRM \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)
    -   [**\_DRM-Schlüssel-ID**](drm-keyid.md)
    -   [**\_DRM-LizenzAcqURL**](drm-licenseacqurl.md)

    Die folgenden Eigenschaften sind optional:

    -   [**\_DRM-Inhalts-ID**](drm-contentid.md)
    -   [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md)

    Darüber hinaus können Sie benutzerdefinierte DRM-Dateiattribute direkt mithilfe des [**DRM \_ DRMHeader-Basisattributs**](drm-drmheader.md) angeben. Sie können beliebige zusätzliche Attribute hinzufügen, z. B. "DRMHeader.RequireSAP", um zusätzliche Informationen zu kommunizieren, die vom Lizenzserver beim Erstellen der Lizenz verwendet werden. Der Lizenzserver muss im Voraus über alle zusätzlichen Eigenschaften informiert sein, die Sie hinzufügen. Es gibt keine Möglichkeit, unbekannte Eigenschaften programmgesteuert zu ermitteln.

11. Schreiben Sie die Datei mithilfe der [**IWMWriter-Schnittstellenmethoden,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) wie an anderer Stelle in dieser Dokumentation beschrieben. Um einen Live-DRM-Stream zu erstellen, schreiben Sie einfach in eine Netzwerksenke. Sie können auch in eine Pushsenke schreiben.
12. Erstellen Sie ggf. mithilfe Windows Media Rights Manager eine Lizenz für die Datei. Diese Aufgabe kann auch von einem Drittanbieterlizenzserver ausgeführt werden. Bei Live-DRM-Szenarien müssen Endbenutzer entweder vor dem Start des Streams oder beim ersten Versuch, eine Verbindung damit herzustellen, eine Lizenz erhalten.

**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

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

[**Lesen von geschützten Dateien**](reading-protected-files.md)
</dt> <dt>

[**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




