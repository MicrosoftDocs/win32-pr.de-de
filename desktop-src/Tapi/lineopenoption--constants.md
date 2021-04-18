---
description: Die lineopenoption- \_ Konstanten listet die verfügbaren Optionen zum Öffnen einer Zeile auf.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: LINEOPENOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365726"
---
# <a name="lineopenoption_-constants"></a>Lineopenoption- \_ Konstanten

Die **lineopenoption- \_ Konstanten** listet die verfügbaren Optionen zum Öffnen einer Zeile auf.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**lineopenoption- \_ Proxy**
</dt> <dd> <dl> <dt>



Die Anwendung ist bereit, Anforderungen von anderen Anwendungen zu verarbeiten, für die die Zeile geöffnet ist.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**lineopenoption- \_ singleaddress**
</dt> <dd> <dl> <dt>



Die Anwendung sollte nur über neue Aufrufe informiert werden, die auf dem Zeilen Gerät erstellt wurden, wenn diese Aufrufe für die Adresse angezeigt werden, die im Element " **dwadressssid** " in der [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) -Struktur angegeben ist, auf die durch den *lpcallparameame-* Parameter verwiesen wird.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum Betrieb dieser Optionen finden Sie unter [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




