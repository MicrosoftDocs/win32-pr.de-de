---
description: Im folgenden finden Sie die Qualifizierer, mit denen Sie Ansichts Anbieter Klassen definieren.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Spezifische Qualifizierer für den Ansichts Anbieter
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
ms.openlocfilehash: 76f28e4ba3433c168e1d0bf86887ee93df953444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217399"
---
# <a name="qualifiers-specific-to-the-view-provider"></a>Spezifische Qualifizierer für den Ansichts Anbieter

Im folgenden finden Sie die Qualifizierer, mit denen Sie Ansichts Anbieter Klassen definieren.

> [!Note]  
> Die Ansichts Anbieter Klasse unterstützt nur NetBIOS-Namen, wenn Remote Verweise verwendet werden. Wenn Sie eine IP-Adresse oder einen DNS-Namen in einem Remote Verweis verwenden, schlägt die Verbindung mit einem 0x800706ba-Fehler fehl.

 

<dt>

<span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Unmittelbaren**
</dt> <dd>

Datentyp: **boolescher** Wert

Wird zusammen mit Ansichts Zuordnungs Eigenschaften verwendet, um zu verhindern, dass Zuordnungs Verweise einem Sicht Verweis zugeordnet werden.

Im folgenden Beispiel wird die Eigenschaft **GroupComponent** als Zuordnungs Verweis definiert, der nicht in der Sicht Referenz zugeordnet ist.


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**Hiddendefault**
</dt> <dd>

Datentyp: **boolescher** Wert

Standardwert für eine Ansichts Klassen Eigenschaft, die auf einer Quell Klassen Eigenschaft mit einem anderen Standardwert basiert. Die zugrunde liegende Quell Klasse wird von der Ansicht impliziert.

Beispielsweise verfügt die Quell Klasse [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) über eine [boolesche](boolean.md) Eigenschaft **runwiederholtem** , die angibt, ob der Auftrag in regelmäßigen Abständen oder nur einmal ausgeführt werden soll. Der Standardwert von **runwiederholtem** ist für **Win32 \_ ScheduledJob** nicht true, aber für die Ansichts Klasse.


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

<span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**Joinon**
</dt> <dd>

Datentyp: **Zeichenfolge**

Definiert, wie Quell Klassen Instanzen in joinansichts Klassen verknüpft werden. Im folgenden Beispiel wird gezeigt, wie der **joinon** -Qualifizierer verwendet wird, um zwei Quell Klassen zu verknüpfen.


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**Methodsource**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Die Quell Methode, die für die Ansichts Methode ausgeführt werden soll. Eine ähnliche Syntax finden Sie unter [propertysources-Qualifizierer](propertysources-qualifier.md). Die Signatur der Methode muss genau mit der Signatur der Quell Klasse übereinstimmen. Kopieren Sie die Methoden Signatur aus der MOF-Datei, die die Quell Klasse definiert. Im folgenden Beispiel wird eine Methode aus der [**cleareventlog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) -Methode der [**Win32-Datei " \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))" definiert:


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



Dieser Qualifizierer ist nur gültig, wenn er mit Union-Sichten verwendet wird.

</dd> <dt>

<span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**Postjoinfilter**](postjoinfilter-qualifier.md)
</dt> <dd>

Datentyp: **Zeichenfolge**

WQL-Abfrage zum Filtern von Instanzen, nachdem Sie in einer joinklasse verknüpft wurden.

</dd> <dt>

<span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**Propertysources**](propertysources-qualifier.md)
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Quell Eigenschaften, von denen eine Eigenschaft der Ansichts Klasse Daten abruft.

</dd> <dt>

<span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**
</dt> <dd>

Datentyp: **boolescher** Wert

Gibt an, ob Sie eine Union-Klasse definieren. Union-Sichten enthalten Instanzen, die auf der Vereinigung der Quell Instanzen basieren. Sie können z. b. Folgendes deklarieren:


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**Viewsources**](viewsources-qualifier.md)
</dt> <dd>

Datentyp: **Zeichen folgen Array**

WQL-Abfragen (Set of WMI Query Language), die die Quell Instanzen und-Eigenschaften definieren, die in einer bestimmten Ansichts Klasse verwendet werden. Die Positions Entsprechung aller Array Qualifizierer ist wichtig.

</dd> <dt>

<span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**Viewspaces**](viewspaces-qualifier.md)
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Namespaces, in denen sich die Quell Instanzen befinden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

