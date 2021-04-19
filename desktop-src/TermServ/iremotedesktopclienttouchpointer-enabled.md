---
title: Iremotedesktopclienttouchpointer-aktivierte Eigenschaft
description: Gibt an, ob die Funktion für den Fingerabdruck für das Client Steuerelement der RDP-App aktiviert ist.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Aktivierte Eigenschaften Remotedesktopdienste
- Aktivierte Eigenschaften Remotedesktopdienste, iremotedesktopclienttouchpointer-Schnittstelle
- Iremotedesktopclienttouchpointer-Schnittstelle Remotedesktopdienste, aktivierte Eigenschaft
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342636"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>Iremotedesktopclienttouchpointer:: aktivierte Eigenschaft

Gibt an, ob die Funktion für den Fingerabdruck für das Client Steuerelement der RDP-App aktiviert ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a>Eigenschaftswert

**true** , wenn die Berührungs Zeiger Funktion aktiviert ist. andernfalls **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                      |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| IID<br/>                      | IID \_ iremotedesktopclienttouchpointer ist als 260ec22d-8cbc-44b5-9e88-2a37f 6c93ae9 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iremotedesktopclienttouchpointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

