---
title: IMsRdpClientNonScriptable-SendKeys-Methode
description: Sendet eine Reihe von Tastatureingaben an das Steuerelement. Die Tastatureingaben sind in Scancodeform, d.&a0;b. den Tastaturdaten der tatsächlichen physischen Tasten.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- SendKeys-Remotedesktopdienste
- SendKeys-Remotedesktopdienste , IMsRdpClientNonScriptable-Schnittstelle
- IMsRdpClientNonScriptable-Schnittstelle Remotedesktopdienste , SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste , IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste , SendKeys-Methode
- SendKeys-Remotedesktopdienste , IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste , SendKeys-Methode
- SendKeys-Remotedesktopdienste , IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste , SendKeys-Methode
- SendKeys-Methode Remotedesktopdienste , IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste , SendKeys-Methode
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530f74bdab808ce6cad6f777d12da932db073ddec022e007eb73fabc538fab20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118855318"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a>IMsRdpClientNonScriptable::SendKeys-Methode

Sendet eine Reihe von Tastatureingaben an das Steuerelement. Die Tastatureingaben sind in Scancodeform, d.&a0;b. den Tastaturdaten der tatsächlichen physischen Tasten.

## <a name="syntax"></a>Syntax


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*numKeys* \[ In\]
</dt> <dd>

Die Anzahl der zu sendenden Tastatureingaben. Die maximale Anzahl von Schlüsseln, die in einem Vorgang gesendet werden können, beträgt 20. Die -Methode gibt **E \_ INVALIDARG zurück,** wenn dieser Parameter größer als 20 ist. Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> <dt>

*pbArrayKeyUp* \[ In\]
</dt> <dd>

Ein Array, dessen Größe gleich *numKeys ist.* Ein Element ist **TRUE,** wenn der entsprechende Schlüssel UP und **FALSE ist,** wenn der entsprechende Schlüssel DOWN ist.

</dd> <dt>

*plKeyData* \[ In\]
</dt> <dd>

Ein Array, dessen Größe gleich *numKeys ist.* Das Array enthält Tastatureingabedaten und entspricht dem Wert des *lParam-Parameters* der [WM \_ KEYDOWN-Nachricht.](../inputdev/wm-keydown.md) Die Daten geben die Wiederholungsanzahl, den Scancode, das Flag für erweiterte Schlüssel, den Kontextcode, das vorherige Schlüsselzustandsflag und das Übergangszustandsflag an. Eine Beschreibung der Bits in diesem Array finden Sie unter [WM \_ KEYDOWN](../inputdev/wm-keydown.md).

Das entsprechende Element in *pbArrayKeyUp* gibt an, ob der Schlüssel UP oder DOWN ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie **S \_ OK zurück,** wenn erfolgreich.

## <a name="remarks"></a>Hinweise

Die **SendKeys-Methode** vermischen tastaturanschläge des lokalen Benutzers nicht mit Tastatureingaben, die von der Methode gesendet werden. Alle tastaturanschläge, die an die -Methode übergeben werden, werden in einer einzelnen atomaren Sequenz an die Remotesitzung gesendet.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                               |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable ist als 2f079c4c-87b2-4afd-97ab-20cdb43038ae definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[WM \_ KEYDOWN](../inputdev/wm-keydown.md)
</dt> </dl>

 

