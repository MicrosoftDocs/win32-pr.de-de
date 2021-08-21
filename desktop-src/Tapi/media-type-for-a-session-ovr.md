---
description: Der Medientyp (oder -modus) beschreibt den Typ der ausgetauschten Informationen, z. B. interaktive Stimme. Eine bestimmte Kommunikationssitzung kann mehrere Medientypen umfassen.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Medientyp für eine Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974935baf17652c0376386eea63028ba04eeb886d1f48eba1aaf7f8469a9c374
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002878"
---
# <a name="media-type-for-a-session"></a>Medientyp für eine Sitzung

Der Medientyp (oder -modus) beschreibt den Typ der ausgetauschten Informationen, z. B. interaktive Stimme. Eine bestimmte Kommunikationssitzung kann mehrere Medientypen umfassen.

Dienstanbieter machen tapI und Anwendungen den medientypen oder -typen verfügbar, die sie unterstützen. Informationen zum Abrufen [dieser Daten finden](media-type-ovr.md) Sie in der Übersicht über den Gerätemedientyp.

**TAPI 2.x:** Siehe [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**LINE \_ MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE \_ Constants](./linemediamode--constants.md).

**TAPI 3.x:** Weitere Informationen finden Sie unter [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get \_ Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (returns [**CALLINFOCHANGE \_ CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC \_ MEDIATYPE**), [TAPIMEDIATYPE \_ Constants](tapimediatype--constants.md).

 

 
