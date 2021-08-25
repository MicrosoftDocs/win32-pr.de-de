---
description: Die LINEOPENOPTION-Konstanten \_ listen die verfügbaren Optionen zum Öffnen einer Zeile auf.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: LINEOPENOPTION_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dc6a4780b366b2dce08110ecce40c7140ab1d0956d788dce5a67d5d0501b6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739250"
---
# <a name="lineopenoption_-constants"></a>LINEOPENOPTION-Konstanten \_

Die **LINEOPENOPTION-Konstanten \_** listen die verfügbaren Optionen zum Öffnen einer Zeile auf.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_LINEOPENOPTION-PROXY**
</dt> <dd> <dl> <dt>



Die Anwendung ist bereit, Anforderungen von anderen Anwendungen zu verarbeiten, bei denen die Zeile geöffnet ist.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**
</dt> <dd> <dl> <dt>



Die Anwendung sollte nur dann über neue Aufrufe informiert werden, die auf dem Zeilengerät erstellt wurden, wenn diese Aufrufe unter der Adresse angezeigt werden, die im **dwAddressID-Member** in der [**LINECALLPARAMS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) angegeben ist, auf die der *lpCallParams-Parameter* zeigt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zum Betrieb dieser Optionen finden Sie unter [**lineOpen.**](/windows/desktop/api/Tapi/nf-tapi-lineopen)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




