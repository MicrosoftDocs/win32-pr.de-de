---
UID: NF:ntw.EtwEventUnregister
title: EtwEventUnregister-Funktion
description: Aufheben der Registrierung eines Ereignisses.
old-location: ''
ms.assetid: na
ms.date: 02/20/2018
ms.keywords: EtwEventUnregister
ms.topic: reference
req.header: ntetw.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 10, version 1803 [desktop apps \| UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntetw.h
api_name:
- EtwEventUnregister
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: f2918aa3eb5ca3440496aa1f6ef51363045d5b8704b8b6fca059e68ba19a112d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070100"
---
# <a name="etweventunregister-function"></a>EtwEventUnregister-Funktion


## <a name="description"></a>Beschreibung


<b>EtwEventUnregister</b> aufheben die Registrierung eines Ereignisses.
            

Anbieter können diese Funktion nur über ihre <a href="/windows/desktop/ETW/controlcallback">ControlCallback-Funktion</a> aufrufen.


## <a name="parameters"></a>Parameter




### <a name="reghandle-in"></a>RegHandle [in]

Handle für ein Ereignis.


## <a name="returns"></a>Gibt zurück



Gibt ein HRESULT zurück.





## <a name="remarks"></a>Hinweise



## <a name="see-also"></a>Weitere Informationen