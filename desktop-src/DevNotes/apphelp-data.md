---
description: Enthält Informationen zu AppHelp-Daten.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: APPHELP_DATA Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338888"
---
# <a name="apphelp_data-structure"></a>AppHelp- \_ Datenstruktur

Enthält Informationen zu AppHelp-Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**dwFlags**
</dt> <dd>

Dieser Parameter kann einen der folgenden Werte aufweisen:

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

**dwschwere Grad**
</dt> <dd>

Dieser Parameter kann apptype \_ None (0) sein.

</dd> <dt>

**dwhtmlhelpid**
</dt> <dd>

Der HTML-Hilfe Bezeichner.

</dd> <dt>

**szappname**
</dt> <dd>

Der Anwendungsname.

</dd> <dt>

**trexe**
</dt> <dd>

Die [**tagref**](tagref.md) der entsprechenden ausführbaren Datei.

</dd> <dt>

**szURL**
</dt> <dd>

Die URL für den AppHelp Online-Link.

</dd> <dt>

**szlink**
</dt> <dd>

Der Linktext für **szURL**.

</dd> <dt>

**szapptitle**
</dt> <dd>

Der Titel für die AppHelp-Nachricht.

</dd> <dt>

**szcontact**
</dt> <dd>

Die Kontaktinformationen des Anbieters.

</dd> <dt>

**szdetails**
</dt> <dd>

Die ausführliche AppHelp-Nachricht.

</dd> <dt>

**dwdata**
</dt> <dd>

Benutzerdefinierte Daten, die von der Anwendung verwaltet werden.

</dd> <dt>

**bspentry**
</dt> <dd>

Dieser Member ist **true** , wenn sich dieser Eintrag in der Service Pack Datenbank befindet, andernfalls **false** .

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbreadapphelpdetailsdata**](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




