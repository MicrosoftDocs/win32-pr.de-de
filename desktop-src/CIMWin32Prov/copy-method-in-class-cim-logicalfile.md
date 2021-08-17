---
description: 'Copy-Methode der CIM_LogicalFile Klasse: Die Copy-Methode kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den vom Eingabeparameter angegebenen Speicherort.'
ms.assetid: 643946e4-5d32-4839-ae1f-80ec7cede429
ms.tgt_platform: multiple
title: Copy-Methode der CIM_LogicalFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9decb093a78817e36dbaed1e904406c73b3b66fb0c6c3bfb7701ecdf44986b8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419816"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a>Copy-Methode der CIM \_ LogicalFile-Klasse

Die **Copy-Methode** kopiert die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist, an den vom Eingabeparameter angegebenen Speicherort.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* \[ In\]
</dt> <dd>

Vollqualifizierter Name der Zieldatei (oder des Zielverzeichnisses).

Beispiel: "c: \\ temp \\ newdirectory"

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Erfolg.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Zugriff verweigert:

</dd> <dt>

**Nicht angegebener Fehler**
</dt> <dd>

8

Nicht angegebener Fehler.

</dd> <dt>

**Ungültiges Objekt**
</dt> <dd>

9

Ungültiges Objekt.

</dd> <dt>

**Das Objekt ist bereits vorhanden.**
</dt> <dd>

10

Das Objekt ist bereits vorhanden.

</dd> <dt>

**Dateisystem, nicht NTFS**
</dt> <dd>

11

Dateisystem, nicht NTFS.

</dd> <dt>

**Plattform nicht NT/Windows 2000**
</dt> <dd>

12

Plattform nicht Windows.

</dd> <dt>

**Laufwerk nicht identisch**
</dt> <dd>

13

Laufwerk nicht identisch.

</dd> <dt>

**Verzeichnis nicht leer**
</dt> <dd>

14

„Verzeichnis ist nicht leer.“

</dd> <dt>

**Freigabeverletzung**
</dt> <dd>

15

Freigabeverletzung.

</dd> <dt>

**Ungültige Startdatei**
</dt> <dd>

16

Ungültige Startdatei.

</dd> <dt>

**Nicht privileg**
</dt> <dd>

17

Die Berechtigung wurde nicht gehalten.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

Ungültiger Parameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[CIM \_ LogicalFile](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

