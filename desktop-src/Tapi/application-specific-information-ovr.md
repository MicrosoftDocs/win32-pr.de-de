---
description: Anwendungsspezifische Informationen ermöglichen es Anwendungen, alle anderen Informationen über eine Sitzung über TAPI zu übergeben. Diese Informationen werden nicht von TAPI interpretiert, und die Verwendung wird vollständig von den Anwendungen definiert.
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: Anwendungsspezifische Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369113"
---
# <a name="application-specific-information"></a>Anwendungsspezifische Informationen

Anwendungsspezifische Informationen ermöglichen es Anwendungen, alle anderen Informationen über eine Sitzung über TAPI zu übergeben. Diese Informationen werden nicht von TAPI interpretiert, und die Verwendung wird vollständig von den Anwendungen definiert.

Wenn anwendungsspezifische Informationen von einer Anwendung geändert werden, sendet TAPI alle anderen Anwendungen mit Monitor-oder Besitzer Berechtigungen für die Sitzung ein Ereignis, das angibt, dass eine Änderung aufgetreten ist.

Nicht alle Dienstanbieter unterstützen die Verwendung dieser Informationen.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*dwappspecific* Member von *lpcallinfo*), [**linesetappspecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**line \_ CallInfo**](./line-callinfo.md) Message (*dwParam1* auf linecallinfostate \_ AppSpecific festgelegt).

**TAPI 3. x:** Siehe [**itcallinfo:: get \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**itcallinfo::p UT \_ callinfolong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**cil \_ AppSpecific** Member von [**CallInfo \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
