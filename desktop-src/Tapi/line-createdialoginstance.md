---
description: Die TSPI LINE \_ CREATEDIALOGINSTANCE-Nachricht bewirkt, dass TAPI eine Zuordnung zwischen dem Dienstanbieter und einer Instanz der \_ IMSPI-AnbieterGenericDialog-Funktion erstellt, die im Kontext der Anwendung ausgeführt wird.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: LINE_CREATEDIALOGINSTANCE Meldung (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e670a0dbcdde82721e5441b95983d5852e821cc981062947a0d6b76639ad762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873500"
---
# <a name="line_createdialoginstance-message"></a>LINE \_ CREATEDIALOGINSTANCE-Meldung

Die TSPI **LINE \_ CREATEDIALOGINSTANCE-Nachricht** bewirkt, dass TAPI eine Zuordnung zwischen dem Dienstanbieter und einer Instanz der [**GENERISCHENPI-AnbietergenericDialog-Funktion \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) erstellt, die im Kontext der Anwendung ausgeführt wird, die die asynchrone TSPI-Funktion aufgerufen hat, die durch den *dwRequestID-Parameter* der [**STRUKTUR OEMSPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) identifiziert wurde, auf die von *lpTUISPICreateDialogInstanceParams* verwiesen wird.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hProvider* 
</dt> <dd>

Das ProviderHandle, das dem Dienstanbieter als Parameter für [**\_ TSPI-AnbieterEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)bereitgestellt wird.

</dd> <dt>

*lpTUISPICreateDialogInstanceParams* 
</dt> <dd>

Zeiger auf eine [**STRUKTURENSPICREATEDIALOGINSTANCEPARAMS-Struktur.**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**DIALOGSSPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

