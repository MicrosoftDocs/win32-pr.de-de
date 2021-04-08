---
title: Win32_SessionBrokerFarmAccount-Klasse
description: Die Win32- \_ Klasse "sessionbrokerfarmaccount" ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar. | Win32_SessionBrokerFarmAccount-Klasse
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount-Klasse Remotedesktopdienste
- Win32_SessionBrokerFarmAccount Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761850"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a>Win32 \_ sessionbrokerfarmaccount-Klasse

\[Die Win32-Klasse " **\_ sessionbrokerfarmaccount** " ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.\]

Definiert ein Sitzungs Broker-Farmkonto.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ sessionbrokerfarmaccount** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ sessionbrokerfarmaccount** " verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                          |
|:------------------------------------------------------------|:-------------------------------------|
| [**DeleteEx**](deleteex-win32-sessionbrokerfarmaccount.md) | Löscht das Farmkonto.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ sessionbrokerfarmaccount** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccountDomain**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Name der Domäne, zu der das Farmkonto gehört.

</dd> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Name des Farm Kontos.

</dd> <dt>

**Accountpassword**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Kennwort des Farm Kontos.

</dd> <dt>

**AccountSPN1**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der erste Dienst Prinzipal Name (Service Principal Name, SPN), der dem Farmkonto zugeordnet ist.

</dd> <dt>

**AccountSPN2**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zweite SPN, der dem Farmkonto zugeordnet ist.

</dd> <dt>

**Computerdnsname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der DNS-Name des Computers, der dem Farmkonto zugeordnet ist.

</dd> <dt>

**Farmname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name der Sitzungs Broker Farm.

</dd> <dt>

**Manuell**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob das Kennwort für das Konto manuell aktualisiert wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                              |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

