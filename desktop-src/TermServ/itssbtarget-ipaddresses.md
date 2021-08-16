---
title: ITsSbTarget-IpAddresses-Eigenschaft
description: Ruft die externen IP-Adressen des Ziels ab oder gibt sie an.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- TargetExternalIpAddresses-Remotedesktopdienste
- TargetExternalIpAddresses-Eigenschaft Remotedesktopdienste , ITsSbTarget-Schnittstelle
- TargetExternalIpAddresses-Eigenschaft Remotedesktopdienste , ITsSbTarget-Schnittstelle
- IpAddresses-Remotedesktopdienste
- IpAddresses-Eigenschaft Remotedesktopdienste , ITsSbTarget-Schnittstelle
- ITsSbTarget-Schnittstelle Remotedesktopdienste , IpAddresses-Eigenschaft
- IpAddresses-Eigenschaft Remotedesktopdienste , ITsSbTargetEx-Schnittstelle
- ITsSbTargetEx-Schnittstelle Remotedesktopdienste , IpAddresses-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ff06e60f125590154a17cb7467deae3611a617b684e9068439c9e15609d8fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351252"
---
# <a name="itssbtargetipaddresses-property"></a>ITsSbTarget::IpAddresses (Eigenschaft)

Ruft die externen IP-Adressen des Ziels ab oder gibt sie an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf ein Array von [**TSSD \_ ConnectionPoint-Strukturen,**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) die die externen IP-Adressen des Ziels empfangen.

Ein Zeiger auf eine **DWORD-Variable,** die die Anzahl externer IP-Adressen im *sockaddr-Parameter* enthält. Wenn die Anzahl der Adressen unbekannt ist, übergeben Sie *sockaddr* als **NULL.** Die -Methode gibt die Anzahl der [**TSSD \_ ConnectionPoint-Strukturen**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) zurück, die für die Zuordnung im Array erforderlich sind, auf das der *sockaddr-Parameter zeigt.*

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wurde früher als **TargetExternalIpAddresses** in Windows Server 2008 R2 bezeichnet.

Wenn die Anzahl externer IP-Adressen unbekannt ist, können Sie diese Methode aufrufen, bei der *sockaddr auf* **NULL festgelegt ist.** Die -Methode gibt dann im *numAddresses-Parameter* die Anzahl der [**TSSD \_ ConnectionPoint-Strukturen**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) zurück, die zum Empfangen aller externen IP-Adressen erforderlich sind. Ordnen Sie das Array *für sockaddr* basierend auf dieser Zahl zu, und rufen Sie dann erneut die -Methode auf, indem Sie *sockaddr* auf das neu zugeordnete Array und *numAddresses* auf die Zahl festlegen, die vom ersten Aufruf zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterstützte Mindestversion (Client)<br/></td>
<td>Nicht unterstützt<br/></td>
</tr>
<tr class="even">
<td>Unterstützte Mindestversion (Server)<br/></td>
<td>Windows Server 2012<br/></td>
</tr>
<tr class="odd">
<td>Idl<br/></td>
<td><dl> <dt>Sbtsv.idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget ist wie:
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 auf Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





