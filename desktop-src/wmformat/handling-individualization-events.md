---
title: Behandeln von Individualisierungsereignissen
description: Behandeln von Individualisierungsereignissen
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows Medienformat-SDK, Behandlung von Individualisierungsereignissen
- Windows Medienformat-SDK, Individualisierungsereignisse
- Advanced Systems Format (ASF), Behandlung von Individualisierungsereignissen
- ASF (Advanced Systems Format), Behandlung von Individualisierungsereignissen
- Advanced Systems Format (ASF), Individualisierungsereignisse
- ASF (Advanced Systems Format), Individualisierungsereignisse
- Digital Rights Management (DRM), Behandlung von Individualisierungsereignissen
- DRM (Digital Rights Management), Behandlung von Individualisierungsereignissen
- Digital Rights Management (DRM), Individualisierungsereignisse
- DRM (Digital Rights Management), Individualisierungsereignisse
- Individualisierungsereignisse
- Ereignisse,Individualisierungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895710558c58fca108915ad1a73a0354c1fb39feb662fa3e2c698dadbe4cbe76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433616"
---
# <a name="handling-individualization-events"></a>Behandeln von Individualisierungsereignissen

Wenn eine DRM-fähige Anwendung versucht, eine geschützte Datei zu öffnen, untersucht die DRM-Komponente das [**DRM \_ DRMHeader \_ IndividualizedVersion-Attribut**](drm-drmheader-individualizedversion.md) in der Datei, das die Mindestversionsebene angibt, die für den Zugriff auf den Inhalt erforderlich ist. Alle Ebenen der DRM-Komponente funktionieren mit allen Versionen 7.0 und höher von Windows Media Player und dem Windows Media Format SDK. Wenn die individualisierte Versionsebene der DRM-Komponente niedriger als die erforderliche Version ist, sendet die DRM-Komponente ein **WMT \_ NEEDS \_ INDIVIDUALIZATION-Ereignis** an die [**IWMStatusCallback::OnStatus-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) der Anwendung. Die Anwendung muss dann eine Meldung oder ein Dialogfeld anzeigen, in der Benutzer aufgefordert werden, das Sicherheitsupgrade zu starten oder abzubricht. Diese Aufforderung ist erforderlich, da Benutzer aus Datenschutzgründen ihre Berechtigung erteilen müssen, bevor ein Sicherheitsupgrade auf ihrem Computer installiert wird.

> [!Note]  
> Der Header des Inhalts gibt nur die ersten beiden Ziffern für DRM \_ DRMVersion \_ IndividualizedVersion an. Anders ausgedrückt: Um eine DRM-Komponente der Ebene 2.2.0.1 zu erfordern, enthält der Header "2.2".

 

Um das Sicherheitsupgrade zu starten und/oder die Individualisierung auszulösen, rufen Sie die [**IWMDRMReader::Individualize-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) auf, bei der *der dwFlags-Parameter* auf 1 festgelegt ist.

Sie müssen das **WMT \_ INDIVIDUALIZE-Ereignis** in Ihrer Anwendung behandeln. Dieses Ereignis wird mehrmals von der DRM-Komponente mit dem im *pValue-Parameter* angegebenen Status des Individualisierungsprozesses ausgelöst, der in einen Zeiger auf eine [**WM \_ INDIVIDUALIZE \_ STATUS-Struktur**](wm-individualize-status.md) umformt wird.

Nachdem die DRM-Komponente erfolgreich individualisiert wurde, erhält die Anwendung ein **WMT \_ NO RIGHTS \_ \_ EX-Ereignis,** das angibt, dass die Anwendung jetzt mit dem Erwerb einer Lizenz für den Inhalt fortfahren kann.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Behandeln von Lizenzerwerbsereignissen**](handling-license-acquisition-events.md)
</dt> <dt>

[**Individualisieren von DRM-Anwendungen**](individualizing-drm-applications.md)
</dt> <dt>

[**IWMDRMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




