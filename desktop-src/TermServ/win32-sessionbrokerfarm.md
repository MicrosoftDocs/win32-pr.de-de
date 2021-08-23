---
title: Win32_SessionBrokerFarm-Klasse
description: Definiert die Abfrage für eine Sitzungsbrokerfarm.
ms.assetid: 55a2a7ea-e891-4723-b919-ee3c908eaffb
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarm-Klassen-Remotedesktopdienste
- Win32_SessionBrokerFarm -Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarm
- Win32_SessionBrokerFarm.PluginName
- Win32_SessionBrokerFarm.FarmName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab65d00cd4be793556929d3049db549ad8ab9729d1e2e2752e550c3e2cf357d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422510"
---
# <a name="win32_sessionbrokerfarm-class"></a>Win32 \_ SessionBrokerFarm-Klasse

Definiert die Abfrage für eine Sitzungsbrokerfarm.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARM_Prov"), AMENDMENT]
class Win32_SessionBrokerFarm
{
  string PluginName;
  string FarmName;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SessionBrokerFarm-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SessionBrokerFarm-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name der Sitzungsbrokerfarm, die abgefragt werden muss.

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des Plug-Ins.

</dd> </dl>

## <a name="examples"></a>Beispiele

Die folgende Abfragezeichenfolge veranschaulicht, wie die **Win32 \_ SessionBrokerFarm-Klasse** in einer Abfrage verwendet wird.


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerFarm WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

