---
description: Gibt an, ob eine Netzwerkadresse einem angegebenen Typ und Format entspricht.
title: NCM_GETADDRESS Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977880"
---
# <a name="ncm_getaddress-message"></a>NCM- \_ GetAddress-Nachricht

Gibt an, ob eine Netzwerkadresse einem angegebenen Typ und Format entspricht.


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*PV* \[ in, out\]
</dt> <dd>Ein Zeiger auf eine <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> -Struktur zum Empfangen von Netzwerk Adressinformationen in der analysierten Form, wenn das Adressformat und der Typ im von *HWND* angegebenen Steuerelement überprüft werden. Die aufrufenden Anwendung ist dafür verantwortlich, den Arbeitsspeicher für diese Struktur zuzuordnen.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte vom Typ **HRESULT** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ invalidArg**</dt> </dl>               | Die aufrufenden Anwendung konnte eine [**NC- \_ Adress**](/windows/win32/api/shellapi/ns-shellapi-nc_address) Struktur nicht zuordnen.<br/> |
| <dl> <dt>**Fehler \_ beim \_ Puffer.**</dt> </dl> | Der Ausgabepuffer ist zu klein, um die analysierte Netzwerkadresse zu speichern.<br/>                           |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>   | Die Netzwerk Adress Zeichenfolge ist nicht von einem beliebigen Typ angegeben.<br/>                                  |
| <dl> <dt>**Fehler \_ erfolgreich**</dt> </dl>              | Der Vorgang wurde durchgeführt.<br/>                                                             |
| <dl> <dt>**S \_ false**</dt> </dl>                    | Es gibt keine Adresse im Netzwerk Adress Steuerelement, das überprüft werden soll.<br/>                           |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **NCM \_ GetAddress** -Nachricht, um eine Netzwerkadresse in einem Netzwerk Adress Steuerelement mit einer voreingestellten Netzwerkadresse zu überprüfen. Verwenden Sie zum Instanziieren die in shellapi. h definierte Klasse **msctls- \_ netaddress** . Ruft vor dem Senden dieser Nachricht [**initnetworkaddresscontrol**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) zur Laufzeit auf. Dadurch wird die Bibliothek der allgemeinen Steuerelemente initialisiert, die das Netzwerk Adress Steuerelement enthält.

Diese Nachricht Ruft die Netzwerk Adress Zeichenfolge aus einem Netzwerk Adress Steuerelement ab, analysiert die Zeichenfolge und überprüft, ob die Zeichenfolge mit einer Netzwerk Adresstyp Maske übereinstimmt. Wenn die Zeichenfolge mit der Maske übereinstimmt, gibt die Meldung S \_ OK zurück und gibt die Zeichenfolge in der analysierten Form an die aufrufende Anwendung zurück (einschließlich der Portnummer, der Präfix Länge und anderer Adressinformationen), wobei die [**NC- \_ Adress**](/windows/win32/api/shellapi/ns-shellapi-nc_address) Struktur verwendet wird, auf die von *PV* verwiesen wird Diese Meldung gibt E \_ invalidArg zurück, wenn die aufrufende Anwendung die Struktur nicht zuordnen kann, auf die von *PV* verwiesen wird.

Darstellungen von IP-Adressen (Internet Protocol), Version 4 und 6 (V4/V6) für Dienste und Netzwerke sowie benannte Internet Adressen und Dienste mit Domain Name System-Format (DNS) werden analysiert. Wenn die Netzwerk Adress Zeichenfolge einen benannten Hostnamen (DNS) oder Dienst darstellt, ist der Wert, der im **prefixlength** -Member der [**NC- \_ Adresse**](/windows/win32/api/shellapi/ns-shellapi-nc_address) zurückgegeben wird, 0 (null)

Legen Sie den Netzwerk Adressentyp Mask mithilfe der [**NCM \_ setallowtype**](ncm-setallowtype.md) -Nachricht fest, bevor Sie das **NCM- \_ GetAddress** -Makro senden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NCM- \_ getallowtype**](ncm-getallowtype.md)
</dt> <dt>

[**NETADDR- \_ GetAddress**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




