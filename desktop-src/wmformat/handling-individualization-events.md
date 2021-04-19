---
title: Behandeln von Individualisierungs Ereignissen
description: Behandeln von Individualisierungs Ereignissen
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows Media-Format-SDK, behandeln von Individualisierungs Ereignissen
- Windows Media-Format-SDK, Individualisierungs Ereignisse
- Advanced Systems Format (ASF), behandeln von Individualisierungs Ereignissen
- ASF (Advanced Systems Format), behandeln von Individualisierungs Ereignissen
- Advanced Systems Format (ASF), individualisierungsereignisse
- ASF (Advanced Systems Format), Individualisierungs Ereignisse
- Digital Rights Management (DRM), behandeln von Individualisierungs Ereignissen
- DRM (Digital Rights Management), behandeln von Individualisierungs Ereignissen
- Digital Rights Management (DRM), Individualisierungs Ereignisse
- DRM (Digital Rights Management), Individualisierungs Ereignisse
- Individualisierungs Ereignisse
- Ereignisse, Individualisierungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106337209"
---
# <a name="handling-individualization-events"></a>Behandeln von Individualisierungs Ereignissen

Wenn eine DRM-fähige Anwendung versucht, eine geschützte Datei zu öffnen, untersucht die DRM-Komponente das [**DRM \_ drmHeader \_ Individual Version**](drm-drmheader-individualizedversion.md) -Attribut in der Datei, das die minimale Versions Ebene angibt, die für den Zugriff auf den Inhalt erforderlich ist. Alle Ebenen der DRM-Komponente funktionieren mit allen 7,0 und höheren Versionen von Windows Media Player und dem Windows Media-Format SDK. Wenn die individualisierte Versions Ebene der DRM-Komponente niedriger als die erforderliche Version ist, sendet die DRM-Komponente ein **WMT- \_ \_ Individualisierungs** Ereignis an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode der Anwendung. Die Anwendung muss dann eine Meldung oder ein Dialogfeld anzeigen, in der Benutzer dazu aufgefordert werden, das Sicherheits Upgrade entweder zu starten oder abzubrechen. Diese Eingabeaufforderung ist erforderlich, da Benutzer aus Datenschutzgründen ihre Berechtigung erteilen müssen, bevor ein Sicherheits Upgrade auf dem Computer installiert wird.

> [!Note]  
> Der Header des Inhalts gibt nur die ersten beiden Ziffern für DRM \_ drmversion \_ Individual Version an. Anders ausgedrückt: um eine DRM-Komponente der Ebene 2.2.0.1 anzufordern, würde der Header "2,2" enthalten.

 

Um das Sicherheits Upgrade und/oder die Initialisierung des Auslösers zu starten, müssen Sie die [**iwmdrmreader:: Individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) -Methode aufrufen, wobei der *dwFlags* -Parameter auf 1 festgelegt ist.

Sie müssen das **WMT \_ Individual** -Ereignis in Ihrer Anwendung behandeln. Dieses Ereignis wird von der DRM-Komponente mehrmals ausgelöst, wobei der Status des im *pValue* -Parameter aufgeführten Individualisierungs Vorgangs angegeben wird, der in einen Zeiger auf eine [**WM \_ Individual- \_ Status**](wm-individualize-status.md) Struktur umgewandelt wird.

Nachdem die DRM-Komponente erfolgreich individualisiert wurde, empfängt die Anwendung ein **WMT \_ No \_ Rights \_ Ex** -Ereignis, das angibt, dass die Anwendung jetzt mit dem Erwerb einer Lizenz für den Inhalt fortfahren kann.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Behandeln von Lizenz Erwerbs Ereignissen**](handling-license-acquisition-events.md)
</dt> <dt>

[**Individualisieren von DRM-Anwendungen**](individualizing-drm-applications.md)
</dt> <dt>

[**Iwmdrmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




