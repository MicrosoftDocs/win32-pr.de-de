---
title: Win32_RDFileAssociation-Klasse
description: Stellt eine Dateityp-Zuordnung für eine RemoteApp dar.
ms.assetid: 9ecf6fa5-36f0-4b37-9d59-781b41c1d90c
ms.tgt_platform: multiple
keywords:
- Win32_RDFileAssociation-Remotedesktopdienste
- Win32_RDFileAssociation klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_RDFileAssociation
- Win32_RDFileAssociation.ExtName
- Win32_RDFileAssociation.ProgIdHint
- Win32_RDFileAssociation.IconPath
- Win32_RDFileAssociation.IconIndex
- Win32_RDFileAssociation.IconContents
- Win32_RDFileAssociation.PrimaryHandler
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8327997449527cfb9d2e66429809f14320ac7fe23c5dac455e04883547eabc4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118849975"
---
# <a name="win32_rdfileassociation-class"></a>Win32 \_ RDFileAssociation-Klasse

Stellt eine Dateityp-Zuordnung für eine RemoteApp dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_RDFileAssociation
{
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a>Member

Die **Win32 \_ RDFileAssociation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ RDFileAssociation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ExtName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der Name der Dateinamenerweiterung, z. B. .txt.

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Inhalt des Symbols für diese Dateiassoz.

</dd> <dt>

**IconIndex**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Index des Symbols in der Datei.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Dateipfad zum Symbol für diese Dateiassoz.

</dd> <dt>

**PrimaryHandler**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob diese Zuordnung für einen primären Handler gilt.

</dd> <dt>

**ProgIdHint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Hinweis zum Öffnen von Dokumenten mit dieser Dateiassoz.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root \\ cimv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

 





