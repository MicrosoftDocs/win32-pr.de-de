---
title: IMsRdpClientAdvancedSettings7 EnableSuperPan (Eigenschaft)
description: Gibt einen booleschen Wert an, der angibt, ob SuperPan aktiviert oder deaktiviert ist, oder ruft diesen ab.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- EnableSuperPan-Remotedesktopdienste
- EnableSuperPan-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste , EnableSuperPan-Eigenschaft
- EnableSuperPan-Eigenschaft Remotedesktopdienste , IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste , EnableSuperPan-Eigenschaft
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
ms.openlocfilehash: dd48fbb42f65e42b0cdeee3560c93361c49283eecfa4ee3a792a19f6081b07b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757342"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a>IMsRdpClientAdvancedSettings7::EnableSuperPan (Eigenschaft)

Gibt einen booleschen Wert an, der angibt, ob SuperPan aktiviert oder deaktiviert ist, oder ruft diesen ab. SuperPan ist ein Feature, mit dem Benutzer problemlos im Vollbildmodus durch einen Remotedesktop navigieren können, wenn die Dimensionen des Remotedesktops größer als die Dimensionen des aktuellen Clientfensters sind. Anstatt Scrollleisten zum Navigieren auf dem Desktop zu verwenden, kann der Benutzer auf den Fensterrahmen zeigen, und der Remotedesktop führt automatisch einen Bildlauf in diese Richtung durch. SuperPan unterstützt nicht mehr als einen Monitor.

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

Ein **\_ VARIANT-BOOL-Wert,** der angibt, ob SuperPan aktiviert ist. Der Wert **VARIANT \_ TRUE gibt** an, dass SuperPan aktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 ist als 26036036-4010-4578-8091-0db9a1edf9c3 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





