---
description: Die EXPERTENUMINFO-Struktur stellt Informationen zum Experten zur Verfügung.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: EXPERTENUMINFO-Struktur (Netmon.h)
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
ms.openlocfilehash: 46942f1140cbb5f74685b16e468b68b85221deceeae2509a9d0676261898e238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939037"
---
# <a name="expertenuminfo-structure"></a>EXPERTENUMINFO-Struktur

Die **EXPERTENUMINFO-Struktur** stellt Informationen zum Experten zur Verfügung. Netzwerkmonitor reserviert Speicher für die Struktur und übergibt ihn an den Experten, wenn er die [**Funktion "Expert registrieren"**](register-expert.md) aufruft. Wenn der Experte die Struktur empfängt, muss er alle Informationen ausfüllen, die Netzwerkmonitor werden.

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

**Szname**
</dt> <dd>

Name des Experten.

</dd> <dt>

**szVendor**
</dt> <dd>

Name des Herstellers, der den Experten erstellt.

</dd> <dt>

**szDescription**
</dt> <dd>

Beschreibung des Experten. Der Wert des **szDescription-Members** kann **NULL sein.** Wenn der Name zu lang ist, wird er in der Standardkonfiguration des Viewers abgeschnitten.

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
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG \_ CONFIGURABLE**</dt> </dl>                                          | Der Experte unterstützt Aufrufe der [**Configure-Methode.**](configure.md) <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG \_ VIEWER \_ PRIVATE**</dt> </dl>                                   | Der Experte benötigt eine private (nicht freigegebene) Ereignisanzeige. <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG \_ NO \_ VIEWER**</dt> </dl>                                                  | Der Experte sendet keine Ereignisbenachrichtigungen. <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG \_ ADD \_ ME \_ TO \_ RMC \_ IN \_ SUMMARY**</dt> </dl> | Wenn der Fokus im Zusammenfassungsbereich liegt, wird der Experte im Kontextmenü angezeigt. <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**EXPERT \_ ENUM \_ FLAG ADD ME TO \_ \_ \_ \_ RMC IM \_ \_ DETAIL**</dt> </dl>    | Wenn der Fokus im Detailbereich liegt, wird der Experte im Kontextmenü angezeigt. <br/>  |



 

</dd> <dt>

**hExpert**
</dt> <dd>

Behandeln Sie den Experten. Wenn die **EXPERTENUMINFO-Struktur** zum Registrieren eines Experten verwendet wird, wird der Parameter ignoriert.

</dd> <dt>

**szDllName**
</dt> <dd>

Privates Mitglied; nicht verwenden.

</dd> <dt>

**hModule**
</dt> <dd>

Privates Mitglied; nicht verwenden.

</dd> <dt>

**pRegisterProc**
</dt> <dd>

Privates Mitglied; nicht verwenden.

</dd> <dt>

**pConfigProc**
</dt> <dd>

Privates Mitglied; nicht verwenden.

</dd> <dt>

**pRunProc**
</dt> <dd>

Privates Mitglied; nicht verwenden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




