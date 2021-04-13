---
title: Aktualisieren von Lizenzen
description: Aktualisieren von Lizenzen
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player Online Stores, Aktualisieren von Lizenzen
- Online Stores, Aktualisieren von Lizenzen
- Geben Sie 1 Online Stores ein, aktualisieren Sie Lizenzen.
- Windows Media Player Online Stores, Lizenz Aktualisierung
- Online Stores, Lizenz Aktualisierung
- Typ 1 Online Stores, Lizenz Aktualisierung
- Aktualisieren von Lizenzen
- Lizenzen, aktualisieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314273"
---
# <a name="updating-licenses"></a>Aktualisieren von Lizenzen

Online Stores können Inhalte bereitzustellen, die für einen bestimmten Zeitraum oder bis zu einem bestimmten Zeitpunkt lizenziert sind. Dies wäre normal für Musikinhalte, die als Teil einer Abonnement Dienstvereinbarung bereitgestellt werden. In diesem Fall benötigt der Online Shop eine Gelegenheit, diese Lizenzen zu aktualisieren, bevor Sie ablaufen. dabei wird davon ausgegangen, dass der Benutzer zum erneuern seines Abonnements bezahlt hat. (Wenn der Benutzer das Abonnement nicht erneuert hat, kann es sein, dass die Lizenzen einfach ablaufen lassen.)

Windows Media Player fragt das Content Partner-Plug-in darüber ab, wie weit die vorab Warnung angezeigt werden soll, die der Player über eine zu ablaufende Lizenz bereitstellen sollte. Dies erfolgt durch Aufrufen von [iwmpcontentpartner:: getcontentpartnerinfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), wobei die Konstante g \_ szcontentpartnerinfo \_ licenserefreshadvancewarning über den *bstrinfoname* -Parameter übergeben wird. Um das Plug-in über die ablaufenden Lizenzen zu benachrichtigen, ruft Windows Media Player die [iwmpcontentpartner:: erfrischendes-Lizenz](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense)auf. Dieser Befehl erfordert Parameter, die Details zu der aktualisierten Datei bereitstellen, z. b. ob sich die Datei auf dem Computer des Benutzers befindet, und den Pfad zur Datei. Wenn die Lizenz im Rahmen eines Geräte Synchronisierungs Vorgangs aktualisiert wird, gibt der *preasoncontext* -Parameter den kanonischen Namen des Geräts an.

Wenn Windows Media Player die Aktualisierungs **Lizenz** aufruft, übergibt es ein Cookie, das die Aktualisierungs Anforderung identifiziert. Wenn das Plug-in die Verarbeitung der Update Anforderung abgeschlossen hat, benachrichtigt es Windows Media Player durch den Aufruf von [iwmpcontentpartnercallback:: erfrischendes licensecomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), übergibt das Cookie, die ID des Medien Elements und ein **HRESULT** , das angibt, ob das Update erfolgreich war.

Online Store-Plug-Ins können auch eine Lizenz Überprüfung und Updates als Hintergrundprozess durchführen. Das Plug-in wird von Windows Media Player benachrichtigt, wenn es zulässig ist, Hintergrund Verarbeitungsaufgaben durch Aufrufen von [iwmpcontentpartner:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify)auszuführen. Um dem Plug-in zu signalisieren, dass die Hintergrundverarbeitung gestartet werden soll, übergibt der Spieler den [wmppartnernotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) -Enumerationswert "wmpsnbackgroundprocessingbegin;". um dem Plug-in zu signalisieren, dass die Hintergrundverarbeitung beendet werden soll, übergibt der Spieler den Wert wmpsnbackgroundprocessingend.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für den Typ 1 Online Stores**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




