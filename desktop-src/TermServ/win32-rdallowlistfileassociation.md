---
title: Win32_RDAllowListFileAssociation-Klasse
description: Beschreibt eine veröffentlichte Dateitypzuordnung mit einer RemoteApp.
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Win32_RDAllowListFileAssociation-Klassen-Remotedesktopdienste
- Win32_RDAllowListFileAssociation-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_RDAllowListFileAssociation
- Win32_RDAllowListFileAssociation.ExtName
- Win32_RDAllowListFileAssociation.AppAlias
- Win32_RDAllowListFileAssociation.ProgIdHint
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db555e2a6945a7442830bd72c6dc8ddd27b0d49cdb70852ec10a1a67dec6baea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850199"
---
# <a name="win32_rdallowlistfileassociation-class"></a>Win32 \_ RDAllowListFileAssociation-Klasse

Beschreibt eine veröffentlichte Dateitypzuordnung mit einer RemoteApp.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_RDAllowListFileAssociation
{
  string ExtName;
  string AppAlias;
  string ProgIdHint;
};
```

## <a name="members"></a>Member

Die **Win32 \_ RDAllowListFileAssociation-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ RDAllowListFileAssociation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AppAlias**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Alias der RemoteApp, die der Erweiterung zugeordnet ist.

</dd> <dt>

**ExtName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Name der Erweiterung, z. B. .txt.

</dd> <dt>

**ProgIdHint**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Hinweis zum Öffnen von Dokumenten mit dieser Dateizuordnung

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root \\ cimv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

 





