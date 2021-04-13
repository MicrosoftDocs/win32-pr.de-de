---
description: 'Mit der IWiaDevMgr2:: registereventcallbackclsid-Methode wird eine Anwendung zum Empfangen von Ereignissen registriert, auch wenn die Anwendung nicht ausgeführt wird.'
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'IWiaDevMgr2:: registereventcallbackclsid-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527074"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a>IWiaDevMgr2:: registereventcallbackclsid-Methode

Mit der **IWiaDevMgr2:: registereventcallbackclsid** -Methode wird eine Anwendung zum Empfangen von Ereignissen registriert, auch wenn die Anwendung nicht ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Gibt Registrierungsflags an. Kann auf die folgenden Werte festgelegt werden:



| Registrierungsflag                | Bedeutung                                           |
|----------------------------------|---------------------------------------------------|
| WIA- \_ Register \_ Ereignis \_ Rückruf   | Registrieren Sie sich für das-Ereignis.                           |
| \_ \_ Ereignis Rückruf für die Aufhebung der Registrierung \_ | Löschen Sie die Registrierung für das Ereignis.            |
| WIA \_ - \_ Standard \_ Handler festlegen       | Legen Sie die Anwendung als Standard Ereignishandler fest. |



 

</dd> <dt>

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt einen Geräte Bezeichner an. Übergeben Sie **null** , um für das Ereignis auf allen WIA 2,0-Geräten zu registrieren.

</dd> <dt>

" *Peer-GUID* \[ " in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *GUID \** _

Gibt das Ereignis an, für das die Anwendung registriert wird. Eine Liste der Standard Ereignisse finden Sie unter [WIA-Ereignis](-wia-wia-event-identifiers.md)Bezeichner.

</dd> <dt>

_pClsID * \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *GUID \** _

Zeiger auf die Anwendungs Klassen-ID (_ * CLSID * *). Das WIA 2,0-Laufzeitsystem verwendet die Anwendungs- **CLSID** , um die Anwendung zu starten, wenn ein Ereignis auftritt, das für registriert ist.

</dd> <dt>

*bstrinname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Anwendung an, die für das Ereignis registriert wird.

</dd> <dt>

*bstraudescription* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt eine Textbeschreibung der Anwendung an, die für das Ereignis registriert wird.

</dd> <dt>

*bstricon* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen einer Bilddatei an, die für das Symbol für die Anwendung verwendet werden soll, die für das Ereignis registriert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

WIA 2,0-Anwendungen verwenden diese Methode, um sich für den Empfang von Hardware Geräte Ereignissen zu registrieren. Nachdem **IWiaDevMgr2:: registereventcallbackclsid** aufgerufen wurde, wird die Anwendung für den Empfang von WIA 2,0-Geräte Ereignissen registriert, auch wenn Sie nicht ausgeführt wird.

Wenn das Ereignis auftritt, bestimmt das WIA 2,0-System, welche Anwendung registriert ist, um das Ereignis zu empfangen. Er verwendet die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion und die im *pclsid* -Parameter angegebene CLSID, um eine Instanz der Anwendung zu erstellen, und ruft dann die [**imageeventcallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) -Methode auf, um die Ereignis Informationen an die Anwendung zu übertragen.

Eine Anwendung kann die [**enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md) -Methode aufrufen, um Ereignis Registrierungsinformationen aufzuzählen.

Wenn die Anwendung keine registrierte Component Object Model (com)-Komponente ist und nicht mit der WIA 2,0-Architektur kompatibel ist, verwenden Sie die [**IWiaDevMgr2:: registereventcallbackprogram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) -Methode, um eine Anwendung für Geräte Ereignisse zu registrieren.

> [!Note]  
> In einer Multithreadanwendung gibt es keine Garantie dafür, dass der Rückruf der Ereignis Benachrichtigung für denselben Thread zurückgegeben wird, der den Rückruf registriert hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
