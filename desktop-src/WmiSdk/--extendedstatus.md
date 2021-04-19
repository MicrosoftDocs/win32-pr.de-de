---
description: Wird verwendet, um detaillierte Status-und Fehlerinformationen zu melden.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: __ExtendedStatus-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350169"
---
# <a name="__extendedstatus-class"></a>\_\_ExtendedStatus-Klasse

Die " **\_ \_ ExtendedStatus** "-System Klasse wird verwendet, um detaillierte Status-und Fehlerinformationen zu melden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a>Member

Die **\_ \_ ExtendedStatus** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ ExtendedStatus** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine beliebige benutzerdefinierte Zeichenfolge, die einen Fehler-oder Betriebsstatus beschreibt.

</dd> <dt>

**Vorgang**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Vorgang, der zum Zeitpunkt eines Fehlers oder einer Anomalieerkennung stattfindet. In der Regel legt Windows-Verwaltungsinstrumentation (WMI) diese Eigenschaft auf den Namen einer com-API für die WMI-Methode fest, z. b. die folgende: [**IWbemServices:: kreateinstanceenum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

</dd> <dt>

**Parameter Info**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Parameter, die an einem Fehler oder einer Statusänderung beteiligt sind. Wenn eine Anwendung z. b. versucht, eine Klasse abzurufen, die nicht vorhanden ist, wird diese Eigenschaft auf den Namen der angreifenden Klasse festgelegt.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert den Anbieter, der einen Fehler oder eine Statusänderung auslöst oder meldet. Wenn ein Anbieter nicht beteiligt ist, wird diese Zeichenfolge auf "Windows-Verwaltung" festgelegt.

</dd> <dt>

**Statuscode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Enthält einen Fehler-oder Informations Code für einen Vorgang. Dies kann ein beliebiger Wert sein, der vom Anbieter definiert wird. der Wert 0 (null) ist jedoch normalerweise reserviert, um den Erfolg anzugeben. Diese Eigenschaft wird von [**\_ \_ notifystatus**](--notifystatus.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ ExtendedStatus** -Klasse wird von der [**\_ \_ notifystatus**](--notifystatus.md) -Klasse abgeleitet.

Verwenden Sie die **\_ \_ ExtendedStatus** -Klasse, um Informationen zu melden, die komplexer sind als ein einfacher Ergebniscode. Anbieter können Ihre eigenen Klassen von **\_ \_ ExtendedStatus** ableiten, wenn Sie weitere Eigenschaften benötigen, um die Fehler zu beschreiben.

Die **Statuscode** -Eigenschaft, die von der übergeordneten [**\_ \_ notifystatus**](--notifystatus.md) -Klasse geerbt wurde, ist eine Ganzzahl ohne Vorzeichen, die den Fehler-oder Statuswert darstellt. Wenn Instanzen dieser Klasse von einem dynamischen Anbieter von einer Methode zurückgegeben werden, werden die Eigenschaften " **Statuscode** " und " **Beschreibung** " vom Anbieter festgelegt, und die anderen Eigenschaften werden von WMI festgelegt.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel stammt aus dem [FND: Behandeln von Configuration Manager asynchronen Fehlern mithilfe von WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript-Codebeispiel in der TechNet Gallery, beschreibt die Verwendung von **\_ \_ ExtendedStatus** zum Abrufen von Fehlerinformationen.


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Notifystatus**](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

