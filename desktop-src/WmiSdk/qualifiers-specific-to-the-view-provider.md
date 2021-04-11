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
# <a name="qualifiers-specific-to-the-view-provider"></a><span data-ttu-id="9f4d0-103">Spezifische Qualifizierer für den Ansichts Anbieter</span><span class="sxs-lookup"><span data-stu-id="9f4d0-103">Qualifiers Specific to the View Provider</span></span>

<span data-ttu-id="9f4d0-104">Im folgenden finden Sie die Qualifizierer, mit denen Sie Ansichts Anbieter Klassen definieren.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-104">The following lists the qualifiers use to define View Provider classes.</span></span>

> [!Note]  
> <span data-ttu-id="9f4d0-105">Die Ansichts Anbieter Klasse unterstützt nur NetBIOS-Namen, wenn Remote Verweise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-105">The View provider class only supports NetBIOS names when using remote references.</span></span> <span data-ttu-id="9f4d0-106">Wenn Sie eine IP-Adresse oder einen DNS-Namen in einem Remote Verweis verwenden, schlägt die Verbindung mit einem 0x800706ba-Fehler fehl.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-106">If you use an IP address or a DNS name in a remote reference, then the connection fails with a 0x800706ba error.</span></span>

 

<dt>

<span data-ttu-id="9f4d0-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Unmittelbaren**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Direct**</span></span>
</dt> <dd>

<span data-ttu-id="9f4d0-108">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f4d0-108">Data type: **boolean**</span></span>

<span data-ttu-id="9f4d0-109">Wird zusammen mit Ansichts Zuordnungs Eigenschaften verwendet, um zu verhindern, dass Zuordnungs Verweise einem Sicht Verweis zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-109">Used with view association properties to prevent association references from being mapped to a view reference.</span></span>

<span data-ttu-id="9f4d0-110">Im folgenden Beispiel wird die Eigenschaft **GroupComponent** als Zuordnungs Verweis definiert, der nicht in der Sicht Referenz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-110">The following example defines the property **GroupComponent** as an association reference that is not mapped in the view reference.</span></span>


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span data-ttu-id="9f4d0-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**Hiddendefault**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span></span>
</dt> <dd>

<span data-ttu-id="9f4d0-112">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f4d0-112">Data type: **boolean**</span></span>

<span data-ttu-id="9f4d0-113">Standardwert für eine Ansichts Klassen Eigenschaft, die auf einer Quell Klassen Eigenschaft mit einem anderen Standardwert basiert.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-113">Default value for a view class property based on a source class property with a different default value.</span></span> <span data-ttu-id="9f4d0-114">Die zugrunde liegende Quell Klasse wird von der Ansicht impliziert.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-114">The underlying source class is implied by the view.</span></span>

<span data-ttu-id="9f4d0-115">Beispielsweise verfügt die Quell Klasse [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) über eine [boolesche](boolean.md) Eigenschaft **runwiederholtem** , die angibt, ob der Auftrag in regelmäßigen Abständen oder nur einmal ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-115">For example, the source class [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) has a [boolean](boolean.md) property **RunRepeatedly** that indicates whether the job is to be carried out periodically or one time only.</span></span> <span data-ttu-id="9f4d0-116">Der Standardwert von **runwiederholtem** ist für **Win32 \_ ScheduledJob** nicht true, aber für die Ansichts Klasse.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-116">The default value of **RunRepeatedly** is not True for **Win32\_ScheduledJob**, but is True for the view class.</span></span>


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

<span data-ttu-id="9f4d0-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**Joinon**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span></span>
</dt> <dd>

<span data-ttu-id="9f4d0-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-118">Data type: **string**</span></span>

<span data-ttu-id="9f4d0-119">Definiert, wie Quell Klassen Instanzen in joinansichts Klassen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-119">Defines how source class instances are joined in join view classes.</span></span> <span data-ttu-id="9f4d0-120">Im folgenden Beispiel wird gezeigt, wie der **joinon** -Qualifizierer verwendet wird, um zwei Quell Klassen zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-120">The following example shows how to use the **JoinOn** qualifier to join two source classes.</span></span>


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span data-ttu-id="9f4d0-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**Methodsource**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span></span>
</dt> <dd>

<span data-ttu-id="9f4d0-122">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-122">Data type: **string array**</span></span>

<span data-ttu-id="9f4d0-123">Die Quell Methode, die für die Ansichts Methode ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-123">Source method to execute for the view method.</span></span> <span data-ttu-id="9f4d0-124">Eine ähnliche Syntax finden Sie unter [propertysources-Qualifizierer](propertysources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="9f4d0-124">For similar syntax, see [PropertySources Qualifier](propertysources-qualifier.md).</span></span> <span data-ttu-id="9f4d0-125">Die Signatur der Methode muss genau mit der Signatur der Quell Klasse übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-125">The signature of the method must match the signature of the source class exactly.</span></span> <span data-ttu-id="9f4d0-126">Kopieren Sie die Methoden Signatur aus der MOF-Datei, die die Quell Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-126">Copy the method signature from the MOF file that defines the source class.</span></span> <span data-ttu-id="9f4d0-127">Im folgenden Beispiel wird eine Methode aus der [**cleareventlog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) -Methode der [**Win32-Datei " \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))" definiert:</span><span class="sxs-lookup"><span data-stu-id="9f4d0-127">The example below defines a method from the [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) method of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span></span>


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



<span data-ttu-id="9f4d0-128">Dieser Qualifizierer ist nur gültig, wenn er mit Union-Sichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-128">This qualifier is only valid when it is used with union views.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**Postjoinfilter**](postjoinfilter-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="9f4d0-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f4d0-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-130">Data type: **string**</span></span>

<span data-ttu-id="9f4d0-131">WQL-Abfrage zum Filtern von Instanzen, nachdem Sie in einer joinklasse verknüpft wurden.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-131">WQL query to filter instances after they have been joined in a join class.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**Propertysources**](propertysources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="9f4d0-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f4d0-133">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-133">Data type: **string array**</span></span>

<span data-ttu-id="9f4d0-134">Quell Eigenschaften, von denen eine Eigenschaft der Ansichts Klasse Daten abruft.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-134">Source properties from which a view class property gets data.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**</span></span>
</dt> <dd>

<span data-ttu-id="9f4d0-136">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f4d0-136">Data type: **boolean**</span></span>

<span data-ttu-id="9f4d0-137">Gibt an, ob Sie eine Union-Klasse definieren.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-137">Indicates whether you are defining a union class.</span></span> <span data-ttu-id="9f4d0-138">Union-Sichten enthalten Instanzen, die auf der Vereinigung der Quell Instanzen basieren.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-138">Union views contain instances based on the union of source instances.</span></span> <span data-ttu-id="9f4d0-139">Sie können z. b. Folgendes deklarieren:</span><span class="sxs-lookup"><span data-stu-id="9f4d0-139">For example, you might declare the following:</span></span>


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span data-ttu-id="9f4d0-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**Viewsources**](viewsources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="9f4d0-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f4d0-141">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-141">Data type: **string array**</span></span>

<span data-ttu-id="9f4d0-142">WQL-Abfragen (Set of WMI Query Language), die die Quell Instanzen und-Eigenschaften definieren, die in einer bestimmten Ansichts Klasse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-142">Set of WMI Query Language (WQL) queries that define the source instances and properties used in a specific view class.</span></span> <span data-ttu-id="9f4d0-143">Die Positions Entsprechung aller Array Qualifizierer ist wichtig.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-143">Positional correspondence of all the array qualifiers is important.</span></span>

</dd> <dt>

<span data-ttu-id="9f4d0-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**Viewspaces**](viewspaces-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="9f4d0-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f4d0-145">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="9f4d0-145">Data type: **string array**</span></span>

<span data-ttu-id="9f4d0-146">Namespaces, in denen sich die Quell Instanzen befinden.</span><span class="sxs-lookup"><span data-stu-id="9f4d0-146">Namespaces where the source instances are located.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f4d0-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f4d0-147">Requirements</span></span>



| <span data-ttu-id="9f4d0-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f4d0-148">Requirement</span></span> | <span data-ttu-id="9f4d0-149">Wert</span><span class="sxs-lookup"><span data-stu-id="9f4d0-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9f4d0-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f4d0-150">Minimum supported client</span></span><br/> | <span data-ttu-id="9f4d0-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f4d0-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9f4d0-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f4d0-152">Minimum supported server</span></span><br/> | <span data-ttu-id="9f4d0-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f4d0-153">Windows Server 2008</span></span><br/> |



 

