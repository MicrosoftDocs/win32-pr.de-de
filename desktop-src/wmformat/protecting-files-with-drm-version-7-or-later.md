---
title: Schützen von Dateien mit DRM-Version 7 oder höher
description: Schützen von Dateien mit DRM-Version 7 oder höher
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- Windows Media-Format-SDK, erstellen geschützter Dateien
- Windows Media-Format-SDK, geschützte Dateien
- Advanced Systems Format (ASF), erstellen geschützter Dateien
- ASF (Advanced Systems Format), erstellen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF), wmstubdrm. lib
- ASF (Advanced Systems Format), wmstubdrm. lib
- Wmstubdrm. lib, erstellen geschützter Dateien
- Wmstubdrm. lib, geschützte Dateien
- Digital Rights Management (DRM), wmstubdrm. lib
- DRM (Digital Rights Management), wmstubdrm. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee809ea73401f22e4554e74c2ecb8855a0384e0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106339262"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>Schützen von Dateien mit DRM-Version 7 oder höher

Verwenden Sie zum Schützen von Dateien mit Windows Media DRM Version 7 oder höher die [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) -Methode des Writer-Objekts, um DRM-Attribute festzulegen. Da DRM Version 7 und höhere Versionen eindeutige Lizenzen für jede geschützte Datei oder jeden Satz von Dateien aktivieren, verfügt die **iwmdrmwriter** -Schnittstelle auch über Methoden zum Erstellen von Schlüsseln. Diese Methoden werden nur aus Gründen der praktische bereitgestellt.

Führen Sie die folgenden Schritte aus, um die DRM-Dateien mit der DRM-Version 7 oder höher zu schützen:

1.  Verknüpfen Sie wmstubdrm. lib, und aufheben Sie ggf. die Verknüpfung von Wmvcore. lib.
2.  Rufen Sie die [**wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) -Funktion auf, um den DRM-Writer zu erstellen. Das erste Argument ist reserviert und muss auf **null** festgelegt werden.
3.  Legen Sie ein Profil fest, das der Writer verwenden soll, indem Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) oder [**iwmwriter:: setprofilebyid**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)aufrufen. Sie müssen ein Profil im Writer festlegen, bevor Sie DRM-Attribute festlegen. DRM wird nur für Profile unterstützt, die die Windows Media Audio oder Windows Media Video Codecs verwenden.
4.  Rufen Sie die [**iwmdrmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) -Schnittstelle des Writer-Objekts ab.
5.  Nennen Sie [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , und legen Sie " [**\_ Advanced \_ DRM**](use-advanced-drm.md) " auf " **true**" fest.
6.  Wenn Sie einen neuen schlüsselseed generieren müssen, rufen Sie [**iwmdrmwriter:: generatekeyseed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed)auf. In den meisten Fällen verwenden Sie einen zuvor generierten Schlüssel-Seed wieder. Dieser Wert muss geheim bleiben. Sie wird nicht in die Datei geschrieben.
7.  Rufen Sie [**iwmdrmwriter:: generatekeyid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) auf, um eine Schlüssel-ID zu erstellen. Dies ist der zweite Wert, der zum Erstellen des eigentlichen Schlüssels verwendet wird. Im Gegensatz zum Schlüssel-Seed ist die Schlüssel-ID öffentlich und wird in die Datei im DRM-Header im Klartext geschrieben. Erstellen Sie eine neue Schlüssel-ID für jede neue Datei, die Sie erstellen.
8.  Rufen Sie bei Bedarf **iwmdrmwriter:: generatesigningkeypair** auf, um einen öffentlichen und einen privaten Schlüssel zu generieren, der zum Signieren des erweiterten DRM-DRM-Header Objekts verwendet wird. Weitere Informationen zu diesen Schlüsseln finden Sie unter [**iwmdrmwriter:: generatesigningkeypair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).
9.  Rufen Sie ggf. die Werte ab, um das digitale Signatur Objekt des DRM-Headers aufzufüllen. Wenn auf Ihrem System keine funktionierende Version von Windows Media Rights Manager installiert ist, müssen Sie das digitale Signatur Objekt des ASF-Datei Headers konfigurieren, indem Sie die folgenden vier Attribute angeben, die alle von Microsoft abgerufen werden müssen:

    -   [**DRM \_ lasignaturerootcert**](drm-lasignaturerootcert.md)
    -   [**DRM- \_ lasignaturecert**](drm-lasignaturecert.md)
    -   [**DRM \_ lasignaturelicsrvcert**](drm-lasignaturelicsrvcert.md)
    -   [**DRM- \_ lasignatureprivkey**](drm-lasignatureprivkey.md)

    Wenn Sie Windows Media Rights Manager installiert haben, müssen Sie diese Attribute nicht in der Anwendung festlegen. Die DRM-Komponente ruft diese Attribute ab und verwendet Sie, um den Header automatisch zu signieren. Wenn Sie über eine aktivierte Version von Windows Media Rights Manager auf einem anderen Computer verfügen und diese Werte der digitalen Signatur Objekte wieder verwenden möchten, können Sie Sie in der Registrierung finden. Das Lizenzserver Zertifikat wird unter HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs: cert1 gespeichert, und das Stamm Zertifikat wird unter HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs: cert2 gespeichert. Beim Schützen von Dateien mit DRM-Version 7 müssen Sie die Werte dieser Registrierungsschlüssel verwenden. Verwenden Sie für die **DRM- \_ lasignatureprivkey-Eigenschaft** entweder **generatesigningkeysex** (über das Windows Media Rights Manager SDK), oder verwenden Sie den von Windows Media Rights Manager installierten Wert unter HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WM Rights Manager \\ License Server: info \_ Cert0. Verwenden Sie für die **DRM- \_ lasignaturecert** -Eigenschaft entweder **generatesigningkeysex** (über das Windows Media Rights Manager SDK) oder andernfalls den von Windows Media Rights Manager installierten Wert unter HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs: cert0.

10. Nennen Sie [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) so oft wie erforderlich, um das Writer-Objekt zu konfigurieren, mit dem die erforderlichen DRM-Header Attribute nach Bedarf festgelegt werden. Diese Eigenschaften bleiben für die Lebensdauer des Writer-Objekts oder bis zum Zurücksetzen mit einem neuen Wert erhalten. Sie müssen für jede neue Datei, die Sie erstellen, nicht zurückgesetzt werden.

    Die folgenden Eigenschaften sind für das Writer-Objekt erforderlich:

    -   [**DRM \_ headersignprivkey**](drm-headersignprivkey.md)
    -   [**DRM- \_ keyseed**](drm-keyseed.md)
    -   [**DRM- \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)
    -   [**DRM- \_ Schlüssel-ID**](drm-keyid.md)
    -   [**DRM- \_ Lizenz-AcqURL**](drm-licenseacqurl.md)

    Die folgenden Eigenschaften sind optional:

    -   [**DRM- \_ contentid**](drm-contentid.md)
    -   [**DRM- \_ IndividualizedVersion**](drm-individualizedversion.md)

    Außerdem können Sie benutzerdefinierte DRM-Dateiattribute direkt mithilfe des [**DRM- \_ drmHeader**](drm-drmheader.md) -Basis Attributs angeben. Beispielsweise können Sie ein beliebiges zusätzliches Attribut hinzufügen, z. b. "drmHeader. Requirements SAP", um zusätzliche Informationen zu übermitteln, die vom Lizenzserver bei der Erstellung der Lizenz verwendet werden. Der Lizenzserver muss im Voraus über alle zusätzlichen Eigenschaften, die Sie hinzufügen, informiert werden. Es gibt keine Möglichkeit, unbekannte Eigenschaften Programm gesteuert zu ermitteln.

11. Schreiben Sie die Datei mithilfe der [**iwmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) -Schnittstellen Methoden, wie an anderer Stelle in dieser Dokumentation beschrieben. Um einen Live-DRM-Stream zu erstellen, schreiben Sie einfach in eine Netzwerk Senke. Sie können auch in eine Push-Senke schreiben.
12. Erstellen Sie ggf. mithilfe von Windows Media Rights Manager eine Lizenz für die Datei. Diese Aufgabe kann auch von einem Drittanbieter-Lizenzserver ausgeführt werden. Bei Live-DRM-Szenarios müssen Endbenutzer eine Lizenz abrufen, bevor der Datenstrom beginnt, oder wenn Sie zum ersten Mal versuchen, eine Verbindung damit herzustellen.

**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**DRM-Attribut Liste**](drm-attribute-list.md)
</dt> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> <dt>

[**Iwmdrmwriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> <dt>

[**Iwmheaderinfo:: Event Tribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Iwmwriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Geschützte Dateien werden gelesen.**](reading-protected-files.md)
</dt> <dt>

[**Wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




