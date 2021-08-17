---
title: WSMan.GetErrorMessage-Methode (WSManDisp.h)
description: Gibt eine formatierte Zeichenfolge zurück, die den Text einer Fehlernummer enthält.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- GetErrorMessage-Methode Windows Remoteverwaltung
- GetErrorMessage-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung , GetErrorMessage-Methode
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e7f23a5d2678d3df024c78397aaeb6a388d8b75368f329867f6457b9ad4d84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742090"
---
# <a name="wsmangeterrormessage-method"></a>WSMan.GetErrorMessage-Methode

Gibt eine formatierte Zeichenfolge zurück, die den Text einer Fehlernummer enthält. Diese Methode führt denselben  Vorgang wie die Winrm-Befehlszeilen-Winrm-Hilfemsg  *decimal oder hexadezimale Fehlernummer aus.*

## <a name="syntax"></a>Syntax


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*errorNumber* \[ In\]
</dt> <dd>

Eine Fehlermeldungsnummer in dezimaler oder hexadezimaler Form von WinRM, WinHTTP oder anderen Betriebssystemkomponenten.

</dd> <dt>

*errorMessage* \[ out\]
</dt> <dd>

Eine Fehlermeldungszeichenfolge, die wie meldungen formatiert ist, die vom **Winrm-Befehl zurückgegeben** werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die entsprechende C++-Methode ist [**IWSManEx::GetErrorMessage.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wsman**](wsman.md)
</dt> </dl>

 

 





