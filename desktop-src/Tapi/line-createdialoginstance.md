---
description: Die TSPI-Zeile " \_ foratedialoginstance" bewirkt, dass TAPI eine Zuordnung zwischen dem Dienstanbieter und einer Instanz der "tuispi \_ providergenericdialog"-Funktion erstellt, die im Kontext der Anwendung ausgeführt wird.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: LINE_CREATEDIALOGINSTANCE Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351319"
---
# <a name="line_createdialoginstance-message"></a>Zeile "" mit der Meldung "". \_

Die TSPI- **Zeile " \_ foratedialoginstance** " bewirkt, dass TAPI eine Zuordnung zwischen dem Dienstanbieter und einer Instanz der " [**tuispi \_ providergenericdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) "-Funktion erstellt, die im Kontext der Anwendung ausgeführt wird, die die asyndie Chrone TSPI-Funktion, die durch den *dwrequestid-* Parameter der [**tuispikreatedialoginstanceparameginstancepara**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) -Struktur identifiziert wird, auf die von *lptuispikreatedialoginstanceparameams* verwiesen wird.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprovider* 
</dt> <dd>

Das ProviderHandle, das für den Dienstanbieter als Parameter für [**TSPI \_ providerenumdevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)bereitgestellt wird.

</dd> <dt>

*lptuispikreatedialoginstanceparameams* 
</dt> <dd>

Zeiger auf die Struktur " [**tuispikreatedialoginstanceparameginstanceparameginstancepara**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TSPI \_ providerenumdevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**"Tuispikreatedialoginstanceparameginstancepara"**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

