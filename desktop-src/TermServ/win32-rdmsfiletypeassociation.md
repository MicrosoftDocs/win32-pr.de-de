---
title: Win32_RDMSFileTypeAssociation-Klasse
description: Verwaltet eine Dateityp Zuordnung für eine veröffentlichte Anwendung.
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSFileTypeAssociation-Klasse Remotedesktopdienste
- Win32_RDMSFileTypeAssociation Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2e569077bf47a2b0eba63db39ae1e86c39feb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391565"
---
# <a name="win32_rdmsfiletypeassociation-class"></a>Win32 \_ rdmsfiletypeassociation-Klasse

Verwaltet eine Dateityp Zuordnung für eine veröffentlichte Anwendung.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdmsfiletypeassociation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdmsfiletypeassociation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Appalias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Alias der Anwendung ab, die dem Dateityp zugeordnet ist, oder legt ihn fest.

</dd> <dt>

**Extname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Namen der Dateierweiterung ab.

</dd> <dt>

**Iconcontent**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Inhalt des Symbols für den Dateityp ab und legt diesen fest.

</dd> <dt>

**IconIndex**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Index für das Symbol für den Dateityp ab und legt diesen fest.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Pfad zum Symbol für den Dateityp ab und legt diesen fest.

</dd> <dt>

**Isprimaryhandler**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob die Dateityp Zuordnung für den primären Handler gilt, oder legt ihn fest. **True** , wenn die Dateityp Zuordnung für den primären Handler gilt. andernfalls **false**.

</dd> <dt>

**IsPublished**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob dieses freigegebene

Ruft einen Wert ab, der angibt, ob die Dateityp Zuordnung veröffentlicht wird, oder legt ihn fest. **True** , wenn die Dateityp Zuordnung veröffentlicht wird. andernfalls **false**.

</dd> <dt>

**PoolName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Namen des Anwendungs Pools für die Dateityp Zuordnung ab und legt diesen fest.

</dd> <dt>

**Progidhint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft einen Hinweis ab, der Benutzern beim Öffnen der Dateierweiterung behilflich ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> </dl>

 

