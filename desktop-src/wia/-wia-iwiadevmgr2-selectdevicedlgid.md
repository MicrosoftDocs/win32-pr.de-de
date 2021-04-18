---
description: Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'IWiaDevMgr2:: selectdevicedlgid-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347234"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a>IWiaDevMgr2:: selectdevicedlgid-Methode

Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

Gibt das übergeordnete Fenster des Dialog Felds **Gerät auswählen** an.

</dd> <dt>

*LDE vicetype* \[ in\]
</dt> <dd>

Type: **Long**

Gibt an, welcher Typ von WIA 2,0-Gerät verwendet werden soll. Eine Liste der möglichen Werte finden Sie unter [WIA Device Type specifier](-wia-wia-device-type-specifiers.md) .

</dd> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Gibt das Verhalten des Dialog Felds an. Der Wert kann einer der folgenden Werte sein:

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Verwendet das Standardverhalten.

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ Select \_ Device \_ NODEFAULT**


</dt> <dd>

Zeigt das Dialogfeld an, obwohl nur ein entsprechendes Gerät vorhanden ist.

</dd> </dl> </dd> <dt>

*pbstraude viceid* \[ Out, retval\]
</dt> <dd>

Geben Sie Folgendes ein: **BSTR \** _

Zeiger auf eine Zeichenfolge, die die Bezeichnerzeichenfolge des Geräts empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                                  | Beschreibung                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Das Gerät wurde erfolgreich ausgewählt. <br/>                                                          |
| <dl> <dt>**S \_ false**</dt> </dl>                      | Der Benutzer hat das Dialogfeld abgebrochen. <br/>                                                              |
| <dl> <dt>**WIA \_ S \_ kein \_ Gerät \_ verfügbar**</dt> </dl> | Keine WIA 2,0-Hardware Geräte entsprechen den Spezifikationen im *ldebug Type* -Parameter. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird das Dialogfeld **Gerät auswählen** erstellt und angezeigt, sodass der Benutzer ein WIA 2,0-Gerät für die Abbild Erfassung auswählen kann. Wenn ein Gerät erfolgreich ausgewählt wurde, übergibt die **IWiaDevMgr2:: selectdevicedlgid** -Methode die Bezeichnerzeichenfolge über den *pbstraudeviceid* -Parameter an die Anwendung.

Die Anwendung kann die Geräte, die dem Benutzer angezeigt werden, auf bestimmte Typen beschränken, indem Sie die Gerätetypen über den *ltovicetype* -Parameter angeben. Wenn nur ein Gerät die Spezifikation erfüllt, zeigt **IWiaDevMgr2:: selectde vicedlgid** das Dialogfeld **Gerät auswählen** nicht an. Stattdessen wird die Bezeichnerzeichenfolge des Geräts an die Anwendung weitergeleitet, ohne dass das Dialogfeld angezeigt wird. Sie können dieses Verhalten überschreiben und **IWiaDevMgr2:: selectdevicedlgid** erzwingen, um das Dialogfeld anzuzeigen, indem Sie WIA \_ Select \_ Device \_ NODEFAULT als Wert für den *lFlags* -Parameter übergeben. Wenn mehr als ein WIA 2,0-Gerät mit der Spezifikation übereinstimmt, werden alle übereinstimmenden Geräte im Dialogfeld selectdevice angezeigt, sodass der Benutzer eine Auswahl treffen kann.

> [!Note]  
> Es wird empfohlen, dass Anwendungen die Geräte-und Abbild Auswahl über ein Menü Element namens **von Scanner** im Menü **Datei** verfügbar machen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




