---
description: Die Struktur "expertenumschlag Info" enthält Informationen über den Experten.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Expertensequenz Info-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343232"
---
# <a name="expertenuminfo-structure"></a>Expertensequenz Info-Struktur

Die Struktur " **expertenumschlag Info** " enthält Informationen über den Experten. Netzwerkmonitor weist der Struktur Arbeitsspeicher zu und übergibt sie an den Experten, wenn die Register- [**expertenfunktion**](register-expert.md) aufgerufen wird. Wenn der Experte die Struktur empfängt, muss er alle Informationen ausfüllen, die Netzwerkmonitor Anforderungen sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**szName**
</dt> <dd>

Der Name des Experten.

</dd> <dt>

**szvendor**
</dt> <dd>

Der Name des Herstellers, der den Experten erstellt.

</dd> <dt>

**szDescription**
</dt> <dd>

Die Beschreibung des Experten. Der Wert des **szDescription** -Members kann **null** sein. Wenn der Name zu lang ist, wird er in der Standard-Viewer-Konfiguration abgeschnitten.

</dd> <dt>

**Version**
</dt> <dd>

Der Wert muss 0 (null) sein.

</dd> <dt>

**Flags**
</dt> <dd>

Die folgenden Flags beschreiben den Experten.



| Wert                                                                                                                                                                                                                                                    | Bedeutung                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**kennflag für expertenaufzählung \_ \_ \_ konfigurierbar**</dt> </dl>                                          | Der Experte unterstützt Aufrufe der [**configure**](configure.md) -Methode. <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**Experte-Aufzählungs- \_ \_ Flag- \_ Viewer \_ Privat**</dt> </dl>                                   | Der Experte erfordert eine private (nicht freigegebene) Ereignisanzeige. <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**expertenaufzählungs \_ \_ Flag \_ No \_ Viewer**</dt> </dl>                                                  | Der Experte sendet keine Ereignis Benachrichtigungen. <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**expertenaufzählungs \_ \_ Flag " \_ \_ \_ \_ RMC \_ \_ zusammenfassen"**</dt> </dl> | Wenn sich der Fokus im Zusammenfassungs Bereich befindet, wird der Experte im Kontextmenü angezeigt. <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**expertenaufzählungs \_ \_ Flag " \_ \_ \_ \_ RMC \_ im \_ Detail hinzufügen"**</dt> </dl>    | Wenn sich der Fokus im Detailbereich befindet, wird der Experte im Kontextmenü angezeigt. <br/>  |



 

</dd> <dt>

**hexpert**
</dt> <dd>

Handle für den Experten. Wenn die **expertenwert** -Struktur verwendet wird, um einen Experten zu registrieren, wird der-Parameter ignoriert.

</dd> <dt>

**szDllName**
</dt> <dd>

Privates Mitglied; Verwenden Sie nicht.

</dd> <dt>

**HMODULE**
</dt> <dd>

Privates Mitglied; Verwenden Sie nicht.

</dd> <dt>

**pregisterproc**
</dt> <dd>

Privates Mitglied; Verwenden Sie nicht.

</dd> <dt>

**pconfigproc**
</dt> <dd>

Privates Mitglied; Verwenden Sie nicht.

</dd> <dt>

**prunproc**
</dt> <dd>

Privates Mitglied; Verwenden Sie nicht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




