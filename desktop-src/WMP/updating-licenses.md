---
title: Aktualisieren von Lizenzen
description: Aktualisieren von Lizenzen
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player,Aktualisieren von Lizenzen
- Onlineshops,Aktualisieren von Lizenzen
- Typ 1 Onlineshops,Aktualisieren von Lizenzen
- Windows Media Player online stores,license updating
- Onlineshops,Lizenzaktualisierung
- Typ 1 Onlineshops,Lizenzaktualisierung
- Aktualisieren von Lizenzen
- Lizenzen,Aktualisieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182af125021af43b1a08695d00c194ec90c38a543d95123b093d30375e45e0c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117325"
---
# <a name="updating-licenses"></a>Aktualisieren von Lizenzen

Onlineshops können Inhalte liefern, die für einen bestimmten Zeitraum oder bis zu einem bestimmten Datum lizenziert sind. Dies wäre normal für Musikinhalte, die im Rahmen einer Abonnementdienstvereinbarung bereitgestellt werden. In diesem Fall benötigt der Onlineshop die Möglichkeit, diese Lizenzen zu aktualisieren, bevor sie ablaufen. Dabei wird vorausgesetzt, dass der Benutzer für die Verlängerung seines Abonnements bezahlt hat. (Wenn der Benutzer das Abonnement nicht verlängert hat, können die Lizenzen einfach ablaufen lassen.)

Windows Media Player fragt das Inhaltspartner-Plug-In ab, wie viel Vorauswarnung der Player zu einer Lizenz bereitstellen soll, die abläuft. Hierzu ruft es [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo)auf und übergibt die Konstante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning über den *Parameter bstrInfoName.* Um das Plug-In über Lizenzen zu warnen, die ablaufen, ruft Windows Media Player [IWMPContentPartner::RefreshLicense auf.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense) Dieser Aufruf nimmt Parameter an, die Details zur zu aktualisierenden Datei bereitstellen, z. B. ob sich die Datei auf dem Computer des Benutzers befindet, und den Pfad zur Datei. Wenn die Lizenz im Rahmen eines Gerätesynchronisierungsvorgang aktualisiert wird, stellt der *pReasonContext-Parameter* den unbedarften Namen des Geräts zur Verfügung.

Wenn Windows Media Player **RefreshLicence aufruft,** übergibt sie ein Cookie, das die Updateanforderung identifiziert. Wenn das Plug-In die Verarbeitung der Updateanforderung abgeschlossen hat, benachrichtigt es Windows Media Player durch Aufrufen [von IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete)und übergibt das Cookie, die ID des Medienelements und ein **HRESULT,** das angibt, ob das Update erfolgreich war.

Onlineshop-Plug-Ins können auch Lizenzüberprüfungen und Updates als Hintergrundprozess durchführen. Windows Media Player das Plug-In über Zeiten benachrichtigt, zu denen es zulässig ist, Hintergrundverarbeitungsaufgaben durch Aufrufen [von IWMPContentPartner::Notify auszuführen.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) Um dem Plug-In den Start der Hintergrundverarbeitung zu signalisieren, übergibt der Player den [WMPPartnerNotification-Enumerationswert](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin. um dem Plug-In zu signalisieren, die Hintergrundverarbeitung zu beenden, übergibt der Player den Wert wmpsnBackgroundProcessingEnd.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch für Onlineshops vom Typ 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




