---
description: Parameterflags geben Informationen zu verschiedenen Statusflags in Bezug auf eine Kommunikationssitzung an, z. b. ob die Aufruferkennung blockiert werden soll. \_Eine Liste der von TAPI definierten Flags finden Sie unter linecallparamflags-Konstanten.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Parameterflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3adcb8b430045dc41afea4e7f55e5fa4458530b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359029"
---
# <a name="parameter-flags"></a>Parameterflags

Parameterflags geben Informationen zu verschiedenen Statusflags in Bezug auf eine Kommunikationssitzung an, z. b. ob die Aufruferkennung blockiert werden soll. Eine Liste der von TAPI definierten Flags finden Sie unter [linecallparamflags- \_ Konstanten](./linecallparamflags--constants.md) .

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwcallparamflags** -Member von *lpcallinfo*).

**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**cil \_ callparamsflags** -Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
