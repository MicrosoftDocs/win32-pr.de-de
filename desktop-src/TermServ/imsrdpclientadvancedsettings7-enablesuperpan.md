---
title: IMsRdpClientAdvancedSettings7 enablesuperpan (Eigenschaft)
description: Gibt einen booleschen Wert an, der angibt, ob superpan aktiviert oder deaktiviert ist, oder ruft diesen ab.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Enablesuperpan-Eigenschaft Remotedesktopdienste
- Enablesuperpan-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, enablesuperpan (Eigenschaft)
- Enablesuperpan-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, enablesuperpan (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742136"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a>IMsRdpClientAdvancedSettings7:: enablesuperpan (Eigenschaft)

Gibt einen booleschen Wert an, der angibt, ob superpan aktiviert oder deaktiviert ist, oder ruft diesen ab. Superpan ist ein Feature, mit dem Benutzer problemlos im Vollbildmodus auf einem Remote Desktop navigieren können, wenn die Dimensionen des Remote Desktops größer sind als die Dimensionen des aktuellen Client Fensters. Anstatt Scrollleisten zum Navigieren im Desktop zu verwenden, kann der Benutzer auf den Fensterrahmen zeigen, und der Remote Desktop führt in dieser Richtung automatisch einen Bildlauf durch. Superpan unterstützt nicht mehr als einen Monitor.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein **Variant- \_ boolescher** Wert, der angibt, ob superpan aktiviert ist. Der Wert **Variant \_ true** gibt an, dass superpan aktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





