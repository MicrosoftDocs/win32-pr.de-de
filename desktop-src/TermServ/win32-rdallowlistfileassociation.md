---
title: Win32_RDAllowListFileAssociation-Klasse
description: Beschreibt eine veröffentlichte Dateityp Zuordnung zu einer RemoteApp.
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Win32_RDAllowListFileAssociation-Klasse Remotedesktopdienste
- Win32_RDAllowListFileAssociation Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 4acbc74b5b0dab228a5c625863b4fcd0574b5f96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476698"
---
# <a name="win32_rdallowlistfileassociation-class"></a>Win32 \_ rdallowlistfileassociation-Klasse

Beschreibt eine veröffentlichte Dateityp Zuordnung zu einer RemoteApp.

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

Die **Win32 \_ rdallowlistfileassociation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdallowlistfileassociation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Appalias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Alias der RemoteApp, die der Erweiterung zugeordnet ist.

</dd> <dt>

**Extname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Name der Erweiterung, z. b. ". txt".

</dd> <dt>

**Progidhint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Hinweis zum Öffnen von Dokumenten mit dieser Datei Zuordnung

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. MOF</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

 





