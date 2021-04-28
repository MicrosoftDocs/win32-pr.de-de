---
description: 'IWiaDevMgr2::SelectDeviceDlgID-Methode: Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardwaregerät für die Imageerfassung auswählen kann.'
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: IWiaDevMgr2::SelectDeviceDlgID-Methode (Wia.h)
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
ms.openlocfilehash: a4279bef86d761ed0eb7d90ad3b8dee46e0f17f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106818"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a>IWiaDevMgr2::SelectDeviceDlgID-Methode

Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardwaregerät für die Imageerfassung auswählen kann.

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

*hwndParent* \[ In\]
</dt> <dd>

Typ: **HWND**

Gibt das übergeordnete Fenster des Dialogfelds **Gerät auswählen** an.

</dd> <dt>

*lDeviceType* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt an, welcher WIA 2.0-Gerätetyp verwendet werden soll. Eine Liste der möglichen Werte finden Sie unter [WIA-Gerätetypspezifizierer.](-wia-wia-device-type-specifiers.md)

</dd> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt das Verhalten des Dialogfelds an. Der Wert kann einer der folgenden Sein:

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Verwendet das Standardverhalten.

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**


</dt> <dd>

Zeigt das Dialogfeld an, obwohl nur ein übereinstimmendes Gerät vorhanden ist.

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[ out, retval\]
</dt> <dd>

Typ: **BSTR \***

Zeiger auf eine Zeichenfolge, die die Bezeichnerzeichenfolge des Geräts empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                                  | Beschreibung                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Das Gerät wurde erfolgreich ausgewählt. <br/>                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | Der Benutzer hat das Dialogfeld abgebrochen. <br/>                                                              |
| <dl> <dt>**WIA \_ S KEIN GERÄT \_ \_ \_ VERFÜGBAR**</dt> </dl> | Keine WIA 2.0-Hardwaregeräte entsprechen den Im *lDeviceType-Parameter angegebenen* Spezifikationen. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt und zeigt das **Dialogfeld Gerät** auswählen an, damit der Benutzer ein WIA 2.0-Gerät für die Bilderfassung auswählen kann. Wenn ein Gerät erfolgreich ausgewählt wurde, übergibt die **IWiaDevMgr2::SelectDeviceDlgID-Methode** seine Bezeichnerzeichenfolge über den *parameter pbstrDeviceID* an die Anwendung.

Die Anwendung kann die dem Benutzer angezeigten Geräte auf bestimmte Typen beschränken, indem sie die Gerätetypen über den *Parameter lDeviceType* angibt. Wenn nur ein Gerät die Spezifikation erfüllt, zeigt **IWiaDevMgr2::SelectDeviceDlgID** das Dialogfeld **Gerät** auswählen nicht an. Stattdessen wird die Bezeichnerzeichenfolge des Geräts an die Anwendung übergeben, ohne das Dialogfeld anzuzeigen. Sie können dieses Verhalten außer Kraft setzen und **IWiaDevMgr2::SelectDeviceDlgID** zwingen, das Dialogfeld anzuzeigen, indem Sie WIA SELECT DEVICE NODEFAULT als Wert für den \_ \_ \_ *lFlags-Parameter* übergeben. Wenn mehr als ein WIA 2.0-Gerät der Spezifikation entspricht, werden alle übereinstimmenden Geräte im Dialogfeld AuswählenGeräte angezeigt, damit der Benutzer eines auswählen kann.

> [!Note]  
> Es wird empfohlen, dass Anwendungen die Geräte- und Bildauswahl über ein Menüelement namens **From scanner** im Menü **Datei verfügbar** machen.

 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




