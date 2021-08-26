---
description: Parameterflags stellen Informationen zu einer Vielzahl von Statusflags für eine Kommunikationssitzung zur Verfügung, z. B. ob die Anruferidentifikation blockiert werden soll. Eine Liste der durch TAPI definierten Flags finden Sie unter \_ LINECALLPARAMFLAGS-Konstanten.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Parameterflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf663ea4ff6121f3e130f9c2a2e4c3c1f86f8611be8cc3fef3762adc535e84bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959860"
---
# <a name="parameter-flags"></a>Parameterflags

Parameterflags stellen Informationen zu einer Vielzahl von Statusflags für eine Kommunikationssitzung zur Verfügung, z. B. ob die Anruferidentifikation blockiert werden soll. Eine Liste der durch TAPI definierten Flags finden Sie unter [ \_ LINECALLPARAMFLAGS-Konstanten.](./linecallparamflags--constants.md)

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2.x:** Siehe [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallParamFlags-Member** von *lpCallInfo*).

**TAPI 3.x:** Siehe [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLPARAMSFLAGS-Member** von [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
