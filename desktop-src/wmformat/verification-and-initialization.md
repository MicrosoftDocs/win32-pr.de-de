---
title: Überprüfung und Initialisierung
description: Überprüfung und Initialisierung
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- SDK für Windows Media-Format, Überprüfung
- SDK für Windows Media-Format, Initialisierung
- Digital Rights Management (DRM), Überprüfung
- DRM (Digital Rights Management), Überprüfung
- Digital Rights Management (DRM), Initialisierung
- DRM (Digital Rights Management), Initialisierung
- Erweiterte APIs für den DRM-Client, Überprüfung
- Erweiterte Client-APIs, Überprüfung
- Erweiterte APIs für den DRM-Client, Initialisierung
- Erweiterte Client-APIs, Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314309"
---
# <a name="verification-and-initialization"></a>Überprüfung und Initialisierung

Führen Sie die folgenden Schritte aus, um zu überprüfen, ob die Transaktion zulässig ist, und um ein Objekt zu initialisieren, das den Inhalt entschlüsselt:

1.  Wenn Sie bereits über die Schlüssel-ID für den Inhalt verfügen, fahren Sie mit Schritt 5 fort.
2.  Rufen Sie die [**wmkreateeditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) -Funktion auf, um ein Metadaten-Editor-Objekt zu erstellen und eine Instanz der [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) -Schnittstelle des Objekts abzurufen.
3.  Ruft **IWMMetadataEditor:: QueryInterface** auf, um eine Instanz der [**iwmdrmeditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) -Schnittstelle abzurufen.
4.  Aufrufen von [**iwmdrmeditor:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) zum Abrufen der **DRM- \_ drmHeader- \_ keyid** -Eigenschaft.
5.  Initialisieren Sie die erweiterten APIs für den Windows Media DRM-Client, indem Sie die [**wmdrmstartup**](wmdrmstartup.md) -Funktion aufrufen.
6.  Rufen Sie die [**wmdrmkreateprotectedprovider**](wmdrmcreateprotectedprovider.md) -Funktion auf, um ein sicheres Anbieter Objekt zu erstellen, und rufen Sie eine Instanz der [**iwmdrmprovider**](iwmdrmprovider.md) -Schnittstelle dieses Objekts ab.
7.  Rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md) auf, um ein Lizenz Verwaltungs Objekt zu erstellen und eine Instanz seiner [**iwmdrmlicensemanagement**](iwmdrmlicensemanagement.md) -Schnittstelle abzurufen.
8.  Nennen Sie [**iwmdrmlicenaberation**](iwmdrmlicensemanagement-createlicenseenumeration.md), und übergeben Sie dabei die Schlüssel-ID und das Recht, das die Aktionen bestimmt, die mit dem Inhalt ausgeführt werden sollen, nachdem er in eine Transaktion aufgenommen wurde. Dieser Befehl ruft eine Instanz der [**iwmdrmlicense**](iwmdrmlicense.md) -Schnittstelle ab, die verwendet werden kann, um alle übereinstimmenden Lizenzen aufzuzählen.
9.  Rufen Sie [**iwmdrmlicense:: getinclusionlist**](iwmdrmlicense-getinclusionlist.md) auf, um die Liste der autorisierten Inhalts Schutzsysteme (CPS) abzurufen, die vom Lizenz Aussteller angegeben werden.
10. Analysieren Sie die Aufnahme Liste, um zu bestätigen, dass die GUID der Ausgabe-CPS von der Lizenz zugelassen wird.
11. Wenn die gewünschte Export-GUID nicht in der Aufnahme Liste enthalten ist, nennen Sie [**iwmdrmlicense:: GetNext**](iwmdrmlicense-getnext.md) , um die nächste anwendbare Lizenz (sofern vorhanden) abzurufen, und wiederholen Sie die Schritte 9 und 10. Wenn keine Lizenz die gewünschte GUID in der Aufnahme Liste aufweist, kann der Export nicht ausgeführt werden.
12. Rufen Sie [**iwmdrmlicense:: kreatesecuredecryptor**](iwmdrmlicense-createsecuredecryptor.md) auf, um ein Entschlüsselungs-Objekt zu erstellen. Übergeben Sie das Anwendungs Zertifikat exportieren. Dieser Befehl stellt einen Zeiger auf eine Instanz der [**iwmdrmentschlüsselungsschnittstelle**](iwmdrmdecrypt.md) des Entschlüsselungs-Objekts und ein binäres Objekt bereit, das den Ausgangswert enthält. Zurzeit wird nur die Windows Media **DRM- \_ \_ Schutztyp \_ RC4** -Konstante als Argument für den *dwFlags* -Parameter unterstützt.
13. Verwenden Sie das RSA OAEP-Verschlüsselungsschema, um den Initialisierungs Vektor zu entschlüsseln.
14. Verwenden Sie die von Microsoft bereitgestellte ASF-Bibliotheks Bibliothek, wenn Sie in den Windows Media DRM-Exportvertrag eintreten, um den Offset für jede Nutzlast in Bytes zu finden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Exportieren von komprimiertem Inhalt**](exporting-compressed-content.md)
</dt> </dl>

 

 




