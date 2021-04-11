---
description: Die Singleton scriptingstandardconsumersetting-Klasse stellt Registrierungsdaten bereit, die allen Instanzen der activescripteventconsumer Standard-Consumerklasse gemeinsam sind.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: Scriptingstandardconsumersetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215329"
---
# <a name="scriptingstandardconsumersetting-class"></a><span data-ttu-id="2fdcb-103">Scriptingstandardconsumersetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="2fdcb-103">ScriptingStandardConsumerSetting class</span></span>

<span data-ttu-id="2fdcb-104">Die Singleton **scriptingstandardconsumersetting** -Klasse stellt Registrierungsdaten bereit, die allen Instanzen der [**activescripteventconsumer**](activescripteventconsumer.md) Standard-Consumerklasse gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-104">The singleton **ScriptingStandardConsumerSetting** class provides registration data that is common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) standard consumer class.</span></span> <span data-ttu-id="2fdcb-105">Eine **activescripteventconsumer** -Instanz verwendet die Eigenschaften **maximumscripts** und **Timeout** .</span><span class="sxs-lookup"><span data-stu-id="2fdcb-105">An **ActiveScriptEventConsumer** instance uses the **MaximumScripts** and **Timeout** properties.</span></span> <span data-ttu-id="2fdcb-106">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="2fdcb-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2fdcb-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fdcb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fdcb-109">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a><span data-ttu-id="2fdcb-110">Member</span><span class="sxs-lookup"><span data-stu-id="2fdcb-110">Members</span></span>

<span data-ttu-id="2fdcb-111">Die **scriptingstandardconsumersetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2fdcb-111">The **ScriptingStandardConsumerSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="2fdcb-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fdcb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fdcb-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fdcb-113">Properties</span></span>

<span data-ttu-id="2fdcb-114">Die **scriptingstandardconsumersetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-114">The **ScriptingStandardConsumerSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fdcb-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fdcb-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fdcb-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2fdcb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fdcb-118">Qualifizierer: [**maxlen**](standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="2fdcb-118">Qualifiers: [**MaxLen**](standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2fdcb-119">Eine kurze Beschreibung eines Objekts mit einer Zeilen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-119">A short description of an object a one line string.</span></span> <span data-ttu-id="2fdcb-120">Enthält die Zeichenfolge **scriptingstandardconsumersetting** , da es sich hierbei um eine Singleton-Klasse handelt.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-120">Contains the string **ScriptingStandardConsumerSetting** because this is a singleton class.</span></span>

</dd> <dt>

<span data-ttu-id="2fdcb-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fdcb-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fdcb-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2fdcb-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fdcb-124">Eine Textbeschreibung eines-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-124">A text description of an object.</span></span>

</dd> <dt>

<span data-ttu-id="2fdcb-125">**Maximumscripts**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-125">**MaximumScripts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fdcb-126">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fdcb-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2fdcb-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fdcb-128">Maximale Anzahl von Skripts, die ausgeführt werden, bevor ein Consumer eine neue Instanz startet.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-128">Maximum number of scripts that are run before a consumer starts a new instance.</span></span> <span data-ttu-id="2fdcb-129">Wenn Sie Speicher Verluste aus Skripts löschen möchten, fahren Sie den Consumer regelmäßig herunter.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-129">To clear out memory leaks from scripts, shut down the consumer regularly.</span></span> <span data-ttu-id="2fdcb-130">Der Standardwert ist 300.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-130">The default value is 300.</span></span>

</dd> <dt>

<span data-ttu-id="2fdcb-131">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-131">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fdcb-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fdcb-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2fdcb-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fdcb-134">Qualifizierer: [**maxlen**](standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="2fdcb-134">Qualifiers: [**MaxLen**](standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2fdcb-135">Der Bezeichner für das Einstellungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-135">Identifier for the setting object.</span></span>

</dd> <dt>

<span data-ttu-id="2fdcb-136">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-136">**Timeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fdcb-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fdcb-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2fdcb-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2fdcb-139">Qualifizierer: [**Einheiten**](standard-qualifiers.md) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="2fdcb-139">Qualifiers: [**units**](standard-qualifiers.md) ("Minutes")</span></span>
</dt> </dl>

<span data-ttu-id="2fdcb-140">Maximale Anzahl von Minuten, bevor ein Consumer eine neue Instanz startet.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-140">Maximum number of minutes before a consumer starts a new instance.</span></span> <span data-ttu-id="2fdcb-141">Wenn 0 (null), steuert die **maximumscripts** -Eigenschaft die Verbraucher Lebensdauer.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-141">If 0 (zero), the **MaximumScripts** property controls the consumer lifetime.</span></span> <span data-ttu-id="2fdcb-142">Der gültige Bereich für das **Timeout** liegt zwischen 0 und 71.000, und der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2fdcb-142">The valid range for **Timeout** is 0 through 71,000 and the default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fdcb-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fdcb-143">Remarks</span></span>

<span data-ttu-id="2fdcb-144">Die einzelne Instanz der **scriptingstandardconsumersetting** -Klasse befindet sich im root \\ CIMV2-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2fdcb-144">The single instance of the **ScriptingStandardConsumerSetting** class resides in the root\\cimv2 namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fdcb-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fdcb-145">Requirements</span></span>



| <span data-ttu-id="2fdcb-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fdcb-146">Requirement</span></span> | <span data-ttu-id="2fdcb-147">Wert</span><span class="sxs-lookup"><span data-stu-id="2fdcb-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fdcb-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2fdcb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2fdcb-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fdcb-149">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2fdcb-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2fdcb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2fdcb-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fdcb-151">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2fdcb-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="2fdcb-152">Namespace</span></span><br/>                | <span data-ttu-id="2fdcb-153">Stamm \\ Abonnement</span><span class="sxs-lookup"><span data-stu-id="2fdcb-153">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="2fdcb-154">MOF</span><span class="sxs-lookup"><span data-stu-id="2fdcb-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fdcb-155"><dt>Scrcons. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2fdcb-155"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fdcb-156">DLL</span><span class="sxs-lookup"><span data-stu-id="2fdcb-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fdcb-157"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2fdcb-157"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fdcb-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fdcb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fdcb-159">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-159">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[<span data-ttu-id="2fdcb-160">Standard Consumer-Klassen</span><span class="sxs-lookup"><span data-stu-id="2fdcb-160">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="2fdcb-161">Ausführen eines Skripts auf der Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2fdcb-161">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="2fdcb-162">Erstellen eines logischen Consumers</span><span class="sxs-lookup"><span data-stu-id="2fdcb-162">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="2fdcb-163">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="2fdcb-163">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="2fdcb-164">**\_\_Eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="2fdcb-164">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

