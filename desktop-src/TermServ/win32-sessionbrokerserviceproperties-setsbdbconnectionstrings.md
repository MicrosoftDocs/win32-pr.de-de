---
title: Die Methode "stionbdbconnectionstrings" der Win32_SessionBrokerServiceProperties-Klasse
description: Speichert DB-Verbindungs Zeichenfolgen (Primär und sekundär) in der Registrierung.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Methode Remotedesktopdienste der Methode "" der Klasse "Win32_SessionBrokerServiceProperties"
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste, Methode ' Methode ', ' Methode '
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476686"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Die Methode "" der \_ Klasse "sessionbrokerserviceproperties" der Win32-Klasse

Speichert DB-Verbindungs Zeichenfolgen (Primär und sekundär) in der Registrierung.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

"Verbindungs Dienst" für " *recentraldbrdcms* \[ " in\]
</dt> <dd>

Die primäre Verbindungs Zeichenfolge.

</dd> <dt>

*secondaryverbindungs-"stringrecentraldbrdcms* \[ " in\]
</dt> <dd>

Die sekundäre Verbindungs Zeichenfolge.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                         |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ sessionbrokerserviceproperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





