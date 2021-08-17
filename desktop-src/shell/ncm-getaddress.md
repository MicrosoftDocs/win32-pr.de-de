---
description: Gibt an, ob eine Netzwerkadresse einem angegebenen Typ und Format entspricht.
title: NCM_GETADDRESS Meldung (Shellapi.h)
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
ms.openlocfilehash: 27f5beec56a0125d26cc359f40b5033eda1f035f2dec7666725264ec6fd59ba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677968"
---
# <a name="ncm_getaddress-message"></a>NCM \_ GETADDRESS-Nachricht

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

*pv* \[ in, out\]
</dt> <dd>Ein Zeiger auf eine <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> Struktur, um Netzwerkadresseninformationen in analysierter Form zu empfangen, wenn das Adressformat und der Typ im von *hwnd* angegebenen Steuerelement überprüft werden. Die aufrufende Anwendung ist für die Zuweisung des Arbeitsspeichers für diese Struktur verantwortlich.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte vom Typ **HRESULT** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Die aufrufende Anwendung konnte keine [**NC \_ ADDRESS-Struktur**](/windows/win32/api/shellapi/ns-shellapi-nc_address) zuordnen.<br/> |
| <dl> <dt>**FEHLER: \_ \_ UNZUREICHENDER PUFFER**</dt> </dl> | Der Out-Puffer ist zu klein, um die analysierte Netzwerkadresse zu speichern.<br/>                           |
| <dl> <dt>**FEHLER: \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>   | Die Netzwerkadresszeichenfolge hat keinen angegebenen Typ.<br/>                                  |
| <dl> <dt>**FEHLER \_ ERFOLGREICH**</dt> </dl>              | Der Vorgang wurde durchgeführt.<br/>                                                             |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Im Netzwerkadresssteuerelement ist keine Adresse vorhanden, die überprüft werden soll.<br/>                           |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie die **NCM \_ GETADDRESS-Nachricht,** um eine Netzwerkadresse in einem Netzwerkadresssteuerelement anhand einer vordefinierten Netzwerkadresstypmaske zu überprüfen. Verwenden Sie zum Instanziieren die in Shellapi.h definierte Klasse **msctls \_ netaddress.** Rufen Sie [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) zur Laufzeit auf, bevor Sie diese Nachricht senden. Dadurch wird die Bibliothek für allgemeine Steuerelemente initialisiert, die das Netzwerkadresssteuerelement enthält.

Diese Meldung ruft die Netzwerkadresszeichenfolge aus einem Netzwerkadresssteuerelement ab, analysiert die Zeichenfolge und überprüft, ob die Zeichenfolge mit einer Netzwerkadresstypmaske übereinstimmt. Wenn die Zeichenfolge mit der Maske übereinstimmt, gibt die Nachricht S \_ OK zurück und gibt die Zeichenfolge in analysierter Form an die aufrufende Anwendung zurück (einschließlich Portnummer, Präfixlänge und andere Adressinformationen), wobei die [**NC \_ ADDRESS-Struktur**](/windows/win32/api/shellapi/ns-shellapi-nc_address) verwendet wird, auf die pv zeigt. Diese Meldung gibt E \_ INVALIDARG zurück, wenn die aufrufende Anwendung die Struktur, auf die von *pv* gezeigt wird, nicht zuordnen kann.

Darstellungen der IP-Adressen (Internet Protocol) Version 4 und 6 (v4/v6) für Dienste und Netzwerke sowie benannte Internetadressen und Dienste im DNS-Format (Domain Name System) werden analysiert. Wenn die Netzwerkadresszeichenfolge einen benannten Hostnamen (DNS) oder Dienst darstellt, ist der im **PrefixLength-Member** von [**NC \_ ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) zurückgegebene Wert 0 (null).

Legen Sie die Netzwerkadresstypmaske mithilfe der [**NCM \_ SETALLOWTYPE-Nachricht**](ncm-setallowtype.md) fest, bevor Sie das **NCM \_ GETADDRESS-Makro** senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAddress**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




