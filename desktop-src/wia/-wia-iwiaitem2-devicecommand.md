---
description: Gibt einen Befehl für ein Windows WiA 2.0-Hardwaregerät aus.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: IWiaItem2::D eviceCommand-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f70fd7b4a987dac3a079651f2cbc04dc50817ba8a43f8da1449a3f605683ba65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706310"
---
# <a name="iwiaitem2devicecommand-method"></a>IWiaItem2::D eviceCommand-Methode

Gibt einen Befehl für ein Windows WiA 2.0-Hardwaregerät aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pCmdGUID* \[ In\]
</dt> <dd>

Typ: **const \* GUID**

Gibt den Befehl an, der an das WIA 2.0-Gerät gesendet werden soll. Weitere Informationen [**finden Sie unter WIA-Gerätebefehle.**](-wia-wia-device-commands.md)

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf das [**IWiaItem2-Element,**](-wia-iwiaitem2.md) das durch den Befehl erstellt wurde, sofern dies der Fall ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Zusätzlich zu den STANDARDMÄßIGEN COM-Fehlercodes gibt die -Methode möglicherweise den folgenden Wert zurück.



| Rückgabecode                                                                                       | Beschreibung                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ CMDNOTSUPPORTED**</dt> </dl> | Der Befehl ist nicht für die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) implementiert, für die die -Methode aufgerufen wird. Der numerische Wert für diesen Fehler ist noch nicht definiert. <br/> |



 

## <a name="remarks"></a>Hinweise

Das Verhalten dieser Methode ist abhängig von der Kategorie des Knotens, auf dem die Methode aufgerufen wird, unterschiedlich.

Wenn die Anwendung den [**WIA \_ CMD \_ TAKE \_ PICTURE-Befehl**](-wia-wia-device-commands.md) mithilfe der **IWiaItem2::D eviceCommand-Methode** an das Gerät sendet, erstellt das WIA 2.0-Laufzeitsystem ein [**IWiaItem2-Objekt**](-wia-iwiaitem2.md) zur Darstellung des Bilds. Die **IWiaItem2::D eviceCommand-Methode** speichert die Adresse der Schnittstelle im *ppIWiaItem2-Parameter.*

Anwendungen müssen die [IUnknown::Release-Methode für](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) die Schnittstellenzeigen aufrufen, die sie über den *ppIWiaItem2-Parameter* erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
