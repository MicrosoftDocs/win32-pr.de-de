---
description: Ab Windows 7 implementierte Windows-Verwaltungsinstrumentation (WMI) einen Standardmechanismus zum Ermitteln von Profilen mithilfe des CIM-Schemas.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Cross-Namespace Association Traversal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864028"
---
# <a name="cross-namespace-association-traversal"></a><span data-ttu-id="073a5-103">Cross-Namespace Association Traversal</span><span class="sxs-lookup"><span data-stu-id="073a5-103">Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="073a5-104">Ab Windows 7 implementierte Windows-Verwaltungsinstrumentation (WMI) einen Standardmechanismus zum Ermitteln von Profilen mithilfe des CIM-Schemas.</span><span class="sxs-lookup"><span data-stu-id="073a5-104">Starting in Windows 7, Windows Management Instrumentation (WMI) implemented a standard mechanism for discovering profiles by using the CIM schema.</span></span>

<span data-ttu-id="073a5-105">WMI unterstützt die Registrierung von Cross-Namespace Association und Association Profile.</span><span class="sxs-lookup"><span data-stu-id="073a5-105">WMI supports the cross-namespace association traversal and association profile registration.</span></span> <span data-ttu-id="073a5-106">Weitere Informationen zur Profil Registrierung und zur CIM-Standard Implementierung von Association Traversal finden Sie unter DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) )</span><span class="sxs-lookup"><span data-stu-id="073a5-106">For more information about profile registration and the CIM standard implementation of association traversal, see DSP1033 ([https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf))</span></span>

<span data-ttu-id="073a5-107">Zur Unterstützung dieses Features hat die WMI-Infrastruktur die folgenden Schritte durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="073a5-107">To support this feature, the WMI infrastructure did the following:</span></span>

-   <span data-ttu-id="073a5-108">Der Interop-Namespace wurde erstellt: \\ root \\ Interop.</span><span class="sxs-lookup"><span data-stu-id="073a5-108">Created the interop namespace: \\root\\interop.</span></span>
-   <span data-ttu-id="073a5-109">Zulässiger Überlaufender Zuordnungs Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="073a5-109">Allowed cross namespace association traversal.</span></span> <span data-ttu-id="073a5-110">Zuordnungen, die Namespaces überschreiten, unterstützen das Filtern auf Zuordnungs Klassenebene und auf der implementierten Namespace Ebene.</span><span class="sxs-lookup"><span data-stu-id="073a5-110">Associations that cross namespaces support filtering at the association class level and at the implemented namespace level.</span></span>
-   <span data-ttu-id="073a5-111">Die Klassen " [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))", " [**CIM \_ ElementConfiguration**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)" und " [**CIM \_ referencedprofile**](cim-referencedprofile.md) " wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="073a5-111">Added the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile), and [**CIM\_ReferencedProfile**](cim-referencedprofile.md) classes.</span></span>
-   <span data-ttu-id="073a5-112">Die CIM-Schema Version 2.17.1 Kompatibilität wurde implementiert.</span><span class="sxs-lookup"><span data-stu-id="073a5-112">Implemented CIM Schema version 2.17.1 compatibility.</span></span> <span data-ttu-id="073a5-113">Weitere Informationen finden Sie unter [CIM-Schema Kompatibilität](cim-schema-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="073a5-113">For more information, see [CIM Schema Compatibility](cim-schema-compatibility.md).</span></span>

## <a name="interop-namespace"></a><span data-ttu-id="073a5-114">Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="073a5-114">Interop Namespace</span></span>

<span data-ttu-id="073a5-115">Der Interop-Namespace stellt einen allgemeinen Speicherort für eine Client Anwendung bereit, um alle Profile zu ermitteln, die auf einem Computer unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="073a5-115">The interop namespace provides a common location for a client application to discover all of the profiles that are supported on a computer.</span></span> <span data-ttu-id="073a5-116">Profile können verwendet werden, um verschiedene Aspekte eines Betriebssystems, eines Speicherarrays oder einer Datenbank zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="073a5-116">Profiles can be used to manage various aspects of an operating system, storage array, or database.</span></span>

<span data-ttu-id="073a5-117">Alle Interop-Klassen und-Objekte müssen im Namespace "root Interop" definiert werden \\ .</span><span class="sxs-lookup"><span data-stu-id="073a5-117">All interop classes and objects must be defined in the root\\interop namespace.</span></span>

## <a name="cim-classes"></a><span data-ttu-id="073a5-118">CIM-Klassen</span><span class="sxs-lookup"><span data-stu-id="073a5-118">CIM Classes</span></span>

<span data-ttu-id="073a5-119">Die CIM-Klassen, die in der folgenden Liste beschrieben werden, unterstützen die übergreifende Zuordnung der Namespace Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="073a5-119">The CIM classes described in the following list support cross-namespace association traversal.</span></span>

<dl> <dt>

<span data-ttu-id="073a5-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="073a5-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="073a5-121">Wird verwendet, um die Profil Spezifikation zu identifizieren, die als implementiert angekündigt wird.</span><span class="sxs-lookup"><span data-stu-id="073a5-121">Used to identify the profile specification that is advertised as being implemented.</span></span> <span data-ttu-id="073a5-122">Diese Klasse gibt Informationen an, die den Profilnamen, die Organisation und die Version enthalten, mit denen die Implementierung kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="073a5-122">This class specifies information that includes the profile name, organization, and version with which the implementation is compliant.</span></span>

</dd> <dt>

<span data-ttu-id="073a5-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM \_ elementreformstoprofile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span><span class="sxs-lookup"><span data-stu-id="073a5-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span></span>
</dt> <dd>

<span data-ttu-id="073a5-124">Wird verwendet, um Instanzen von Verwaltungs Elementen, die in Profilen definiert sind, mit der [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) -Klasse zuzuordnen, die die spezifischen Profil Spezifikationen identifiziert, die implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="073a5-124">Used to associate instances of management elements that are defined in profiles with the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) class that identifies the particular profile specifications that are implemented.</span></span>

</dd> <dt>

<span data-ttu-id="073a5-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM \_ referencedprofile**](cim-referencedprofile.md)</span><span class="sxs-lookup"><span data-stu-id="073a5-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM\_ReferencedProfile**](cim-referencedprofile.md)</span></span>
</dt> <dd>

<span data-ttu-id="073a5-126">Wird verwendet, um die Beziehung zwischen Profilen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="073a5-126">Used to represent the relationship between profiles.</span></span>

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a><span data-ttu-id="073a5-127">Implementieren von Cross-Namespace Association Traversal</span><span class="sxs-lookup"><span data-stu-id="073a5-127">Implementing Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="073a5-128">Der WMI-Dienst ermöglicht die übergreifende Zuordnung von Namespace Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="073a5-128">The WMI service allows cross-namespace association traversal.</span></span> <span data-ttu-id="073a5-129">WMI stellt den Interop-Namespace zum Registrieren von Profilen bereit und ordnet diese Profile zu, die in verschiedenen Namespaces implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="073a5-129">WMI provides the interop namespace for registering profiles and associating them with profiles that are implemented in different namespaces.</span></span> <span data-ttu-id="073a5-130">Um jedoch den Zuordnungs Durchlauf zu verwenden, müssen Implementierer die profilklassen sowohl im Interop als auch im implementierten Namespace instanziieren.</span><span class="sxs-lookup"><span data-stu-id="073a5-130">However, to use association traversal, implementers must instantiate the profile classes both in the interop and in the implemented namespace.</span></span> <span data-ttu-id="073a5-131">Weitere Informationen finden Sie unter [Schreiben eines Zuordnungs Anbieters für Interop](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="073a5-131">For more information, see [Writing an Association Provider for Interop](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="073a5-132">Zuordnungen, die Namespaces innerhalb derselben Verwaltungs Umgebung überschreiten, müssen sowohl in der Interop als auch in den implementierten Namespaces instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="073a5-132">Associations that cross namespaces within the same management environment must be instantiated in both the interop and implemented namespaces.</span></span> <span data-ttu-id="073a5-133">Andernfalls funktioniert der Zuordnungs Durchlauf nicht.</span><span class="sxs-lookup"><span data-stu-id="073a5-133">Otherwise, association traversal will not work.</span></span> <span data-ttu-id="073a5-134">Beispielsweise muss der Anbieter der Energieprofil Zuordnung sowohl mit root/Interop-als auch mit root/cimv2/Power-Namespaces registriert werden.</span><span class="sxs-lookup"><span data-stu-id="073a5-134">For example, the power profile association provider must be registered with both root/interop and root/cimv2/power namespaces.</span></span> <span data-ttu-id="073a5-135">Der Zuordnungs Durchlauf sollte in der Lage sein, von einem der beiden Namespaces zurück zum anderen zu werden.</span><span class="sxs-lookup"><span data-stu-id="073a5-135">Association traversal should be able to occur from either namespace back to the other.</span></span> <span data-ttu-id="073a5-136">Beispiele für Zuordnungs quersal finden Sie unter [zugreifen auf Daten im Interop-Namespace](accessing-data-in-the-interop-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="073a5-136">For examples of association traversal, see [Accessing Data in the Interop Namespace](accessing-data-in-the-interop-namespace.md).</span></span>

<span data-ttu-id="073a5-137">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="073a5-137">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="073a5-138">Wenn nach dem Upgrade auf Windows 7 Interop-Geräteprofile vorhanden sind, die zuvor im Root/Interop-Namespace installiert waren, werden keine Windows 7-profile installiert.</span><span class="sxs-lookup"><span data-stu-id="073a5-138">After upgrading to Windows 7, if there are interop device profiles that were previously installed in the root/interop namespace, no Windows 7 profiles will be installed.</span></span> <span data-ttu-id="073a5-139">Diese Profil Objekte von Drittanbietern überschreiben das Interop-Schema von Windows 7, um die Funktionalität aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="073a5-139">These third-party profile objects overwrite Windows 7 interop schema to maintain functionality.</span></span> <span data-ttu-id="073a5-140">Außerdem wird die Ereignis-ID 5631 für die WMI-Anwendung aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="073a5-140">Additionally, the WMI application event ID 5631 is recorded.</span></span>

<span data-ttu-id="073a5-141">Um die Windows 7-Interop-Profile zu erhalten, müssen die Windows 7-Version der Datei "Interop. mof" und die zugehörigen MFL-Dateien kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="073a5-141">To get the Windows 7 interop profiles, the Windows 7 version of the Interop.mof file and the related MFL files must be compiled.</span></span> <span data-ttu-id="073a5-142">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="073a5-142">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="073a5-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="073a5-143">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="073a5-144">[**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="073a5-144">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="073a5-145">**CIM \_ elementreformstoprofile**</span><span class="sxs-lookup"><span data-stu-id="073a5-145">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[<span data-ttu-id="073a5-146">**CIM \_ referencedprofile**</span><span class="sxs-lookup"><span data-stu-id="073a5-146">**CIM\_ReferencedProfile**</span></span>](cim-referencedprofile.md)
</dt> <dt>

[<span data-ttu-id="073a5-147">CIM-Schema Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="073a5-147">CIM Schema Compatibility</span></span>](cim-schema-compatibility.md)
</dt> <dt>

[<span data-ttu-id="073a5-148">Schreiben eines Zuordnungs Anbieters für Interop</span><span class="sxs-lookup"><span data-stu-id="073a5-148">Writing an Association Provider for Interop</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

[<span data-ttu-id="073a5-149">Zugreifen auf Daten im Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="073a5-149">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
