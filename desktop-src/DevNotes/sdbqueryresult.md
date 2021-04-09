---
description: Enthält die Ergebnisse der Abfrage der Shimdatenbank nach einer passenden ausführbaren Datei.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Sdbqueryresult-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958282"
---
# <a name="sdbqueryresult-structure"></a>Sdbqueryresult-Struktur

Enthält die Ergebnisse der Abfrage der Shimdatenbank nach einer passenden ausführbaren Datei.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a>Member

<dl> <dt>

**atrexes**
</dt> <dd>

Die **tagref** -Werte der übereinstimmenden ausführbaren Dateien. Beachten Sie, dass die **maximalen SDB- \_ \_ EXEs** als 16 definiert ist.

</dd> <dt>

**adwexeflags**
</dt> <dd>

Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Shimreg \_ \_Shim deaktivieren** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Shimreg \_ \_AppHelp deaktivieren** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Shimreg \_ AppHelp \_ NoUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Shimreg \_ AppHelp \_ Abbrechen** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Shimreg \_ \_SxS deaktivieren** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Shimreg \_ \_Ebene deaktivieren** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Shimreg \_ \_Treiber deaktivieren** (0x00000040)
</dt> </dl> </dd> <dt>

**atrlayer**
</dt> <dd>

Die **tagref** -Werte der übereinstimmenden Ebenen. Beachten Sie, dass die **maximalen SDB- \_ \_ Ebenen** als 8 definiert sind.

</dd> <dt>

**dwlayerflags**
</dt> <dd>

Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Shimreg \_ \_Shim deaktivieren** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Shimreg \_ \_AppHelp deaktivieren** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Shimreg \_ AppHelp \_ NoUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Shimreg \_ AppHelp \_ Abbrechen** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Shimreg \_ \_SxS deaktivieren** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Shimreg \_ \_Ebene deaktivieren** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Shimreg \_ \_Treiber deaktivieren** (0x00000040)
</dt> </dl> </dd> <dt>

**trapphelp**
</dt> <dd>

Der **tagref** -Wert der "AppHelp"-Meldung der entsprechenden ausführbaren Datei.

</dd> <dt>

**dwexecount**
</dt> <dd>

Die Anzahl der Elemente in **atrexes**.

</dd> <dt>

**dwlayercount**
</dt> <dd>

Die Anzahl der Elemente in **atrlayer**.

</dd> <dt>

**guidid darf**
</dt> <dd>

Die GUID der letzten ausführbaren Datei.

</dd> <dt>

**dwFlags**
</dt> <dd>

Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Shimreg \_ \_Shim deaktivieren** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Shimreg \_ \_AppHelp deaktivieren** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Shimreg \_ AppHelp \_ NoUI** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Shimreg \_ AppHelp \_ Abbrechen** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Shimreg \_ \_SxS deaktivieren** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Shimreg \_ \_Ebene deaktivieren** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Shimreg \_ \_Treiber deaktivieren** (0x00000040)
</dt> </dl> </dd> <dt>

**dwcustomsdbmap**
</dt> <dd>

Eine Zuordnung der benutzerdefinierten Shimdatenbanken. Wenn **rgguiddb** gültig ist, werden die entsprechenden Bits festgelegt.

</dd> <dt>

**rgguiddb**
</dt> <dd>

Die GUIDs der Shimdatenbanken. Beachten Sie, dass **Maximale SDB- \_ \_ SDSB** als 16 definiert ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbgetmatchingexe**](sdbgetmatchingexe.md)
</dt> </dl>

 

 




