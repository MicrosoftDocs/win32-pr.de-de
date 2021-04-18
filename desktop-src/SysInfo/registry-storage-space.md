---
description: Es gibt zwar nur wenige technische Einschränkungen hinsichtlich des Typs und der Größe der Daten, die eine Anwendung in der Registrierung speichern kann, aber es gibt bestimmte praktische Richtlinien, die die Systemeffizienz herauf Stufen.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Registrierungs Speicherplatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357810"
---
# <a name="registry-storage-space"></a><span data-ttu-id="ae42a-103">Registrierungs Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="ae42a-103">Registry Storage Space</span></span>

<span data-ttu-id="ae42a-104">Es gibt zwar nur wenige technische Einschränkungen hinsichtlich des Typs und der Größe der Daten, die eine Anwendung in der Registrierung speichern kann, aber es gibt bestimmte praktische Richtlinien, die die Systemeffizienz herauf Stufen.</span><span class="sxs-lookup"><span data-stu-id="ae42a-104">Although there are few technical limits to the type and size of data an application can store in the registry, certain practical guidelines exist to promote system efficiency.</span></span> <span data-ttu-id="ae42a-105">Eine Anwendung sollte Konfigurations-und Initialisierungs Daten in der Registrierung speichern und andere Arten von Daten an einem anderen Ort speichern.</span><span class="sxs-lookup"><span data-stu-id="ae42a-105">An application should store configuration and initialization data in the registry, and store other kinds of data elsewhere.</span></span>

<span data-ttu-id="ae42a-106">Im Allgemeinen sollten Daten, die aus mehr als einem oder zwei Kilobyte (K) bestehen, als Datei gespeichert werden, und es wird auf einen Schlüssel in der Registrierung verwiesen, anstatt als Wert gespeichert zu werden.</span><span class="sxs-lookup"><span data-stu-id="ae42a-106">Generally, data consisting of more than one or two kilobytes (K) should be stored as a file and referred to by using a key in the registry rather than being stored as a value.</span></span> <span data-ttu-id="ae42a-107">Anstatt große Datenelemente in der Registrierung zu duplizieren, sollte eine Anwendung die Daten als Datei speichern und auf die Datei verweisen.</span><span class="sxs-lookup"><span data-stu-id="ae42a-107">Instead of duplicating large pieces of data in the registry, an application should save the data as a file and refer to the file.</span></span> <span data-ttu-id="ae42a-108">Der binäre Code der ausführbaren Datei sollte nie in der Registrierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ae42a-108">Executable binary code should never be stored in the registry.</span></span>

<span data-ttu-id="ae42a-109">Ein Wert Eintrag verwendet viel weniger Registrierungs Raum als ein Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ae42a-109">A value entry uses much less registry space than a key.</span></span> <span data-ttu-id="ae42a-110">Um Speicherplatz zu sparen, sollte eine Anwendung ähnliche Daten als Struktur gruppieren und die Struktur als Wert speichern, anstatt jedes der Strukturmember als separaten Schlüssel zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ae42a-110">To save space, an application should group similar data together as a structure and store the structure as a value rather than storing each of the structure members as a separate key.</span></span> <span data-ttu-id="ae42a-111">(Das Speichern der Daten in Binär Form ermöglicht einer Anwendung das Speichern von Daten in einem Wert, der andernfalls aus mehreren inkompatiblen Typen besteht.)</span><span class="sxs-lookup"><span data-stu-id="ae42a-111">(Storing the data in binary form allows an application to store data in one value that would otherwise be made up of several incompatible types.)</span></span>

<span data-ttu-id="ae42a-112">Sichten der Registrierungsdateien werden im Auslagerungsseiten-Speicher zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ae42a-112">Views of the registry files are mapped in paged pool memory.</span></span>

<span data-ttu-id="ae42a-113">**Windows Server 2008 für 32 Bit, Windows Vista mit SP1 für 32-Bit, Windows Vista, Windows Server 2003, Windows XP:** Sichten der Registrierungsdateien werden im Cache Adressraum des Computers zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ae42a-113">**Windows Server 2008 for 32-bit, Windows Vista with SP1 for 32-bit, Windows Vista, Windows Server 2003, Windows XP:** Views of the registry files are mapped in the computer cache address space.</span></span> <span data-ttu-id="ae42a-114">Daher wird unabhängig von der Größe der Registrierungsdaten nicht mehr als 4 Megabyte (MB) abgerechnet.</span><span class="sxs-lookup"><span data-stu-id="ae42a-114">Therefore, regardless of the size of the registry data, it is not charged more than 4 megabytes (MB).</span></span>

<span data-ttu-id="ae42a-115">Die maximale Größe einer Registrierungs Struktur beträgt 2 GB, mit Ausnahme der Systemstruktur.</span><span class="sxs-lookup"><span data-stu-id="ae42a-115">The maximum size of a registry hive is 2 GB, except for the system hive.</span></span>

<span data-ttu-id="ae42a-116">**Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP:** Es gibt keine expliziten Grenzwerte für die Gesamtmenge des Speicherplatzes, der von Strukturen in auslagertem Pool Speicher und Speicherplatz beansprucht werden kann, obwohl sich System Kontingente möglicherweise auf die tatsächliche maximale Größe auswirken.</span><span class="sxs-lookup"><span data-stu-id="ae42a-116">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** There are no explicit limits on the total amount of space that may be consumed by hives in paged pool memory and in disk space, although system quotas may affect the actual maximum size.</span></span> <span data-ttu-id="ae42a-117">Die maximale Größe einer Registrierungs Struktur ist ab Windows Server 2003 mit Service Pack 2 (SP2) auf 2 GB beschränkt.</span><span class="sxs-lookup"><span data-stu-id="ae42a-117">The maximum size of a registry hive was limited to 2 GB starting with Windows Server 2003 with Service Pack 2 (SP2).</span></span>

<span data-ttu-id="ae42a-118">Die maximale Größe der Systemstruktur wird durch den physischen Speicher eingeschränkt, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae42a-118">The maximum size of the system hive is limited by physical memory as shown in the following table.</span></span> 

| <span data-ttu-id="ae42a-119">System</span><span class="sxs-lookup"><span data-stu-id="ae42a-119">System</span></span>                      | <span data-ttu-id="ae42a-120">Maximale Größe der Systemstruktur</span><span class="sxs-lookup"><span data-stu-id="ae42a-120">Maximum size of the system hive</span></span>                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae42a-121">x86-basierte Systeme</span><span class="sxs-lookup"><span data-stu-id="ae42a-121">x86-based systems</span></span>           | <span data-ttu-id="ae42a-122">50% des physischen Arbeitsspeichers, bis zu 400 MB. **Windows Server 2003 mit SP2, Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP:** 25% des physischen Arbeitsspeichers, bis zu 200 MB.</span><span class="sxs-lookup"><span data-stu-id="ae42a-122">50 percent of physical memory, up to 400 MB.**Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** 25 percent of physical memory, up to 200 MB.</span></span><br/>                                    |
| <span data-ttu-id="ae42a-123">x64-basierte Systeme</span><span class="sxs-lookup"><span data-stu-id="ae42a-123">x64-based systems</span></span>           | <span data-ttu-id="ae42a-124">50% des physischen Arbeitsspeichers, bis zu 1,5 GB. **Windows Server 2003 mit SP2:** 25% des System Arbeitsspeichers, bis zu 200 MB.</span><span class="sxs-lookup"><span data-stu-id="ae42a-124">50 percent of physical memory, up to 1.5 GB.**Windows Server 2003 with SP2:** 25 percent of system memory, up to 200 MB.</span></span><br/> <span data-ttu-id="ae42a-125">**Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP 64-Bit Edition:** 32 MB.</span><span class="sxs-lookup"><span data-stu-id="ae42a-125">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/> |
| <span data-ttu-id="ae42a-126">Intel Itanium-basierte Systeme</span><span class="sxs-lookup"><span data-stu-id="ae42a-126">Intel Itanium-based systems</span></span> | <span data-ttu-id="ae42a-127">50% des physischen Arbeitsspeichers, bis zu 1 GB. **Windows Server 2008, Windows Vista, Windows Server 2003 mit SP2, Windows Server 2003 mit SP1, Windows Server 2003 und Windows XP 64-Bit Edition:** 32 MB.</span><span class="sxs-lookup"><span data-stu-id="ae42a-127">50 percent of physical memory, up to 1 GB.**Windows Server 2008, Windows Vista, Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/>                         |



 

## <a name="windows-2000"></a><span data-ttu-id="ae42a-128">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ae42a-128">Windows 2000</span></span>

<span data-ttu-id="ae42a-129">Registrierungsdaten werden im ausgelagerten Pool gespeichert, einem Bereich von physischem Arbeitsspeicher, der für Systemdaten verwendet wird, die auf den Datenträger geschrieben werden können, wenn Sie nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae42a-129">Registry data is stored in the paged pool, an area of physical memory used for system data that can be written to disk when not in use.</span></span> <span data-ttu-id="ae42a-130">Mit dem Wert **RegistrySizeLimit** wird die maximale Größe des Auslagerungs Pools festgelegt, der von Registrierungsdaten von allen Anwendungen genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae42a-130">The **RegistrySizeLimit** value establishes the maximum amount of paged pool that can be consumed by registry data from all applications.</span></span> <span data-ttu-id="ae42a-131">Dieser Wert befindet sich im folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="ae42a-131">This value is located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

<span data-ttu-id="ae42a-132">Standardmäßig beträgt das Registrierungs Größenlimit 25 Prozent des Auslagerungs Pools.</span><span class="sxs-lookup"><span data-stu-id="ae42a-132">By default, the registry size limit is 25 percent of the paged pool.</span></span> <span data-ttu-id="ae42a-133">(Die Standardgröße des Auslagerungs Pools beträgt 32 MB, also 8 MB.) Das System stellt sicher, dass der Mindestwert von " **RegistrySizeLimit** " 4 MB und der Höchstwert ungefähr 80 Prozent des Werts "Wert von" **paarweise** "ist.</span><span class="sxs-lookup"><span data-stu-id="ae42a-133">(The default size of the paged pool is 32 MB, so this is 8 MB.) The system ensures that the minimum value of **RegistrySizeLimit** is 4 MB and the maximum is approximately 80 percent of the **PagedPoolSize** value.</span></span> <span data-ttu-id="ae42a-134">Wenn der Wert dieses Eintrags größer als 80 Prozent der Größe des Auslagerungs Pools ist, legt das System die maximale Größe der Registrierung auf 80 Prozent der Größe des Auslagerungs Pools fest.</span><span class="sxs-lookup"><span data-stu-id="ae42a-134">If the value of this entry is greater than 80 percent of the size of the paged pool, the system sets the maximum size of the registry to 80 percent of the size of the paged pool.</span></span> <span data-ttu-id="ae42a-135">Dies verhindert, dass die Registrierung Speicherplatz beansprucht, der von Prozessen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ae42a-135">This prevents the registry from consuming space needed by processes.</span></span> <span data-ttu-id="ae42a-136">Beachten Sie, dass durch Festlegen dieses Werts weder Speicherplatz im Auslagerungs Pool belegt wird noch sichergestellt wird, dass der Speicherplatz bei Bedarf verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ae42a-136">Note that setting this value does not allocate space in the paged pool, nor does it assure that the space will be available if needed.</span></span>

<span data-ttu-id="ae42a-137">Die Größe des ausgelagerten Pools wird durch den Wert für den Wert von " **pgedpoolsize** " im folgenden Registrierungsschlüssel bestimmt:</span><span class="sxs-lookup"><span data-stu-id="ae42a-137">The paged pool size is determined by the **PagedPoolSize** value in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

<span data-ttu-id="ae42a-138">Ein Beispiel für die Bestimmung der aktuellen und der maximalen Größe der Registrierung finden Sie unter [bestimmen der Registrierungs Größe](determining-the-registry-size.md).</span><span class="sxs-lookup"><span data-stu-id="ae42a-138">For an example of how to determine the current and maximum sizes of the registry, see [Determining the Registry Size](determining-the-registry-size.md).</span></span>

<span data-ttu-id="ae42a-139">Der maximale Auslagerungs Pool beträgt ungefähr 300.470 MB, sodass die Registrierungs Größenbeschränkung 240-376 MB beträgt.</span><span class="sxs-lookup"><span data-stu-id="ae42a-139">The maximum paged pool is approximately 300,470 MB so the registry size limit is 240-376 MB.</span></span> <span data-ttu-id="ae42a-140">Wenn jedoch der/3GB-Schalter verwendet wird, beträgt die maximale Größe des Auslagerungs Pools 192 MB, sodass die Registrierung maximal 153,6 MB betragen kann.</span><span class="sxs-lookup"><span data-stu-id="ae42a-140">However, if the /3GB switch is used, the maximum paged pool size is 192 MB, so the registry can be a maximum of 153.6 MB.</span></span>

 

 




