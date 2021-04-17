---
title: Win32_RDCentralPublishedFileAssociation-Klasse
description: Informationen für eine Dateierweiterung, die einer Anwendung zugeordnet ist.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFileAssociation-Klasse Remotedesktopdienste
- Win32_RDCentralPublishedFileAssociation Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a0f1c9bf7905504ee3aa2ba6fff7e9804f4747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478849"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a>Win32 \_ rdcentralpublishedfileassociation-Klasse

Informationen für eine Dateierweiterung, die einer Anwendung zugeordnet ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdcentralpublishedfileassociation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdcentralpublishedfileassociation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Appalias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Alias der RemoteApp der Datei Zuordnung.

</dd> <dt>

**Extname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name der Erweiterung (z. b.. txt).

</dd> <dt>

**Farmalias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Alias der RemoteApp-Farm der Datei Zuordnung

</dd> <dt>

**Iconcontent**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Inhalt des Symbols für diese Datei Zuordnung.

</dd> <dt>

**Primaryhandler**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Für die zukünftige Verwendung reserviert. Wird immer " **true**" sein.

</dd> <dt>

**Progidhint**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Hinweise zum Öffnen von Dokumenten mit dieser Datei Zuordnung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | Root \\ CIMV2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub. MOF</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

