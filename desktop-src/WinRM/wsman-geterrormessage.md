---
title: WSMAN. getErrorMessage-Methode (WSManDisp. h)
description: Gibt eine formatierte Zeichenfolge zurück, die den Text einer Fehlernummer enthält.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- GetErrorMessage-Methode Windows-Remoteverwaltung
- GetErrorMessage-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, getErrorMessage-Methode
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
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340697"
---
# <a name="wsmangeterrormessage-method"></a>WSMAN. getErrorMessage-Methode

Gibt eine formatierte Zeichenfolge zurück, die den Text einer Fehlernummer enthält. Diese Methode führt denselben Vorgang aus wie die **WinRM** -Befehlszeile **WinRM helpmsg** *Decimal oder hexadezimale Fehlernummer*.

## <a name="syntax"></a>Syntax


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*errornumber* \[ in\]
</dt> <dd>

Eine Fehlermeldungs Nummer in Dezimal-oder hexadezimal aus WinRM-, WinHTTP-oder anderen Betriebssystemkomponenten.

</dd> <dt>

*ErrorMessage* \[ vorgenommen\]
</dt> <dd>

Eine Fehlermeldungs Zeichenfolge, die wie vom **WinRM** -Befehl zurückgegebene Meldungen formatiert

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die entsprechende C++-Methode ist " [**iwsmanex:: getErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage)".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WSMAN**](wsman.md)
</dt> </dl>

 

 





