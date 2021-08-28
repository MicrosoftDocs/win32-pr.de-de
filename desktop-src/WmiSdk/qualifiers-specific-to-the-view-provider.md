---
description: Im Folgenden werden die Qualifizierer aufgeführt, die zum Definieren von Ansichtsanbieterklassen verwendet werden.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Qualifizierer, die für den Ansichtsanbieter spezifisch sind
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d7890effa0e8edd07edbb9506f88a78ceffc65fcb8d19bf6c8bcf67860a677f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130972"
---
# <a name="qualifiers-specific-to-the-view-provider"></a>Qualifizierer, die für den Ansichtsanbieter spezifisch sind

Im Folgenden werden die Qualifizierer aufgeführt, die zum Definieren von Ansichtsanbieterklassen verwendet werden.

> [!Note]  
> Die View-Anbieterklasse unterstützt NetBIOS-Namen nur bei Verwendung von Remoteverweisen. Wenn Sie eine IP-Adresse oder einen DNS-Namen in einem Remoteverweis verwenden, tritt bei der Verbindung ein 0x800706ba Fehler auf.

 

<dt>

<span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Direkte**
</dt> <dd>

Datentyp: **boolescher Wert**

Wird mit Ansichtszuordnungseigenschaften verwendet, um zu verhindern, dass Zuordnungsverweise einem Sichtverweis zugeordnet werden.

Im folgenden Beispiel wird die **Eigenschaft GroupComponent** als Zuordnungsverweis definiert, der nicht im Sichtverweis zugeordnet ist.


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**
</dt> <dd>

Datentyp: **boolescher Wert**

Standardwert für eine Ansichtsklasseneigenschaft, die auf einer Quellklasseneigenschaft mit einem anderen Standardwert basiert. Die zugrunde liegende Quellklasse wird von der Sicht impliziert.

Die Quellklasse [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) verfügt beispielsweise über die [boolesche](boolean.md) Eigenschaft **RunRepeatedly,** die angibt, ob der Auftrag regelmäßig oder nur einmal ausgeführt werden soll. Der Standardwert von **RunRepeatedly** ist für **Win32 \_ ScheduledJob** nicht True, für die Ansichtsklasse jedoch True.


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**
</dt> <dd>

Datentyp: **string**

Definiert, wie Quellklasseninstanzen in Joinansichtsklassen verknüpft werden. Das folgende Beispiel zeigt, wie der **JoinOn-Qualifizierer** verwendet wird, um zwei Quellklassen zu verbinden.


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Quellmethode, die für die View-Methode ausgeführt werden soll. Eine ähnliche Syntax finden Sie unter [PropertySources-Qualifizierer.](propertysources-qualifier.md) Die Signatur der -Methode muss genau mit der Signatur der Quellklasse übereinstimmen. Kopieren Sie die Methodensignatur aus der MOF-Datei, die die Quellklasse definiert. Im folgenden Beispiel wird eine Methode aus der [**ClearEventLog-Methode**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) von [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))definiert:


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



Dieser Qualifizierer ist nur gültig, wenn er mit Union-Ansichten verwendet wird.

</dd> <dt>

<span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)
</dt> <dd>

Datentyp: **string**

WQL-Abfrage zum Filtern von Instanzen, nachdem sie in eine Joinklasse eingebunden wurden.

</dd> <dt>

<span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Quelleigenschaften, aus denen eine Ansichtsklasseneigenschaft Daten erhält.

</dd> <dt>

<span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**
</dt> <dd>

Datentyp: **boolescher Wert**

Gibt an, ob Sie eine Union-Klasse definieren. Union-Ansichten enthalten -Instanzen, die auf der Vereinigung von Quellinstanzen basieren. Beispielsweise können Sie Folgendes deklarieren:


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Satz von WQL-Abfragen (WMI Query Language), die die Quellinstanzen und -eigenschaften definieren, die in einer bestimmten Ansichtsklasse verwendet werden. Die positionale Entsprechung aller Arrayqualifizierer ist wichtig.

</dd> <dt>

<span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Namespaces, in denen sich die Quellinstanzen befinden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

