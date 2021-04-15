---
title: Itssbtarget-IPADRESSEN (Eigenschaft)
description: Ruft die externen IP-Adressen des Ziels ab oder legt Sie fest.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Targetexternalipadressen-Eigenschaft Remotedesktopdienste
- Targetexternalipadressen-Eigenschaft Remotedesktopdienste, itssbtarget-Schnittstelle
- Targetexternalipadressen-Eigenschaft Remotedesktopdienste, itssbtarget-Schnittstelle
- IPADRESSEN-Eigenschaft Remotedesktopdienste
- IPADRESSEN-Eigenschaft Remotedesktopdienste, itssbtarget-Schnittstelle
- Itssbtarget-Schnittstelle Remotedesktopdienste, IPADRESSEN-Eigenschaft
- IPADRESSEN-Eigenschaft Remotedesktopdienste, itssbtargetex-Schnittstelle
- Itssbtargetex-Schnittstelle Remotedesktopdienste, IPADRESSEN-Eigenschaft
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
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389125"
---
# <a name="itssbtargetipaddresses-property"></a>Itssbtarget:: IPADRESSEN-Eigenschaft

Ruft die externen IP-Adressen des Ziels ab oder legt Sie fest.

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

Ein Zeiger auf ein Array von [**Tssd- \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) -Strukturen, die die externen IP-Adressen des Ziels empfangen.

Ein Zeiger auf eine **DWORD** -Variable, die die Anzahl externer IP-Adressen im *sockaddr* -Parameter enthält. Wenn die Anzahl der Adressen unbekannt ist, übergeben Sie *sockaddr* als **null**. Die-Methode gibt die Anzahl der [**Tssd- \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) -Strukturen zurück, die erforderlich sind, um im Array zuzuordnen, auf das durch den *sockaddr* -Parameter verwiesen wird.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wurde früher als **targetexternalipadressen** in Windows Server 2008 R2 bezeichnet.

Wenn die Anzahl externer IP-Adressen unbekannt ist, können Sie diese Methode mit *sockaddr* -Wert auf **null** festlegen. Die-Methode gibt dann im *numadkleidungs* -Parameter die Anzahl der [**Tssd- \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) -Strukturen zurück, die erforderlich sind, um alle externen IP-Adressen zu erhalten. Weisen Sie das Array für *sockaddr* auf Grundlage dieser Zahl zu, und klicken Sie dann erneut auf die Methode, und legen Sie *sockaddr* auf das neu zugewiesene Array und *numadcookiezeichen* auf die Zahl fest, die vom ersten-Befehl zurückgegeben wird.

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
<td>IDL<br/></td>
<td><dl> <dt>Sbtsv. idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget ist definiert als:
<ul>
<li>16616ecc-272d-411d-b324-126893033856</li>
<li>e85e10ea-db0b-4752-b456-5sd5840901c0 unter Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbtargetex**](itssbtargetex.md)
</dt> <dt>

[**Itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**Tssd- \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





