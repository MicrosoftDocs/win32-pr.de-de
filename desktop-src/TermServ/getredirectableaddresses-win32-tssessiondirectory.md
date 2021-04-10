---
title: Getredirectableadressen-Methode der Win32_TSSessionDirectory-Klasse
description: Ruft die gesamte Liste der für den DNS berechtigten Adressen ab.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Getredirectableadressen-Methode Remotedesktopdienste
- Getredirectableadressen-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, getredirectableadressen-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040126"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Getredirectableadressen-Methode der Win32- \_ Klasse "tssessiondirectory"

Ruft die gesamte Liste der für den DNS berechtigten Adressen ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Kennzeichen *Umleitung* \[ in\]
</dt> <dd>

Typ: **UInt32**

Ein Flag, das angibt, ob die Tokenumleitung verwendet werden soll.

</dd> <dt>

*IP-Adressen* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Die gesamte Liste der IP-Adressen, die für die Umleitung verfügbar sind.

</dd> <dt>

*Adapternames* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Die Liste der Netzwerkadapter Namen, die den für die Umleitung verfügbaren Adressen zugeordnet sind.

</dd> <dt>

*Netkonname* \[ vorgenommen\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Die Liste der Netzwerk Verbindungs Namen, die den für die Umleitung verfügbaren Adressen zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tssessiondirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

