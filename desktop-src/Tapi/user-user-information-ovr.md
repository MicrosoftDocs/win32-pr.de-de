---
description: Benutzerinformationen sind ein Puffer, der von einem Ende einer Verbindung an ein anderes übertragen werden kann. Diese Informationen sind spezifisch für den ISDN Q.931-Standard. Informationen zur Bedeutung und Verwendung dieser Daten finden Sie in der Dokumentation Ihrer Dienstanbieter.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Benutzer-/Benutzerinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203b0b466d1b0b3f9da93cfefc5da737865da3cf5d40921dae6c969bfc9b9752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975290"
---
# <a name="user-user-information"></a>Benutzer-/Benutzerinformationen

Benutzerinformationen sind ein Puffer, der von einem Ende einer Verbindung an ein anderes übertragen werden kann. Diese Informationen sind spezifisch für den ISDN Q.931-Standard. Informationen zur Bedeutung und Verwendung dieser Daten finden Sie in der Dokumentation Ihres Dienstanbieters.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** und **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

**TAPI 3.x: **[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), aufgerufen mit dem **CIB \_ USERUSERINFO-Member** von [**CALLINFO \_ BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
