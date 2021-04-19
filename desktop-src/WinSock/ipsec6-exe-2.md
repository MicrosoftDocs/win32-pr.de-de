---
description: Die Konfiguration von IPSec-Richtlinien und Sicherheits Zuordnungen für IPv6 erfolgt mit Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346940"
---
# <a name="ipsec6exe"></a><span data-ttu-id="a2298-103">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="a2298-103">Ipsec6.exe</span></span>

<span data-ttu-id="a2298-104">Die Konfiguration von IPSec-Richtlinien und Sicherheits Zuordnungen für IPv6 erfolgt mit Ipsec6.exe.</span><span class="sxs-lookup"><span data-stu-id="a2298-104">Configuration of IPSec policies and security associations for IPv6 is done with Ipsec6.exe.</span></span> <span data-ttu-id="a2298-105">Im folgenden finden Sie Ipsec6.exe Unterbefehle:</span><span class="sxs-lookup"><span data-stu-id="a2298-105">The following are Ipsec6.exe subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="a2298-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**dem ipsec6 SP \[** _Schnittstelle_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="a2298-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 sp \[**_Interface_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a2298-107">Zeigt aktive Sicherheitsrichtlinien an.</span><span class="sxs-lookup"><span data-stu-id="a2298-107">Displays active security policies.</span></span> <span data-ttu-id="a2298-108">Zeigt alternativ aktive Sicherheitsrichtlinien für eine bestimmte Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="a2298-108">Alternately, displays active security policies for a specific interface.</span></span>

</dd> <dt>

<span data-ttu-id="a2298-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**dem ipsec6 SA**</span><span class="sxs-lookup"><span data-stu-id="a2298-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 sa**</span></span>
</dt> <dd>

<span data-ttu-id="a2298-110">Zeigt aktive Sicherheits Zuordnungen an.</span><span class="sxs-lookup"><span data-stu-id="a2298-110">Displays active security associations.</span></span>

</dd> <dt>

<span data-ttu-id="a2298-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**dem ipsec6 c \[** _Dateiname (ohne Erweiterung)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="a2298-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a2298-112">Erstellt Dateien, die zum Konfigurieren von Sicherheitsrichtlinien und Sicherheits Zuordnungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2298-112">Creates files used to configure security policy and security associations.</span></span> <span data-ttu-id="a2298-113">Erstellt *filename*. SPD für Sicherheitsrichtlinien und *Dateiname*. sad für Sicherheits Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="a2298-113">Creates *FileName*.spd for security policies and *FileName*.sad for security associations.</span></span> <span data-ttu-id="a2298-114">Verwenden Sie die erstellten Dateien als Vorlagen, um Sicherheitsrichtlinien oder Sicherheits Zuordnungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a2298-114">Use the created files as templates to configure security policies or security associations.</span></span> <span data-ttu-id="a2298-115">Die Dateien können mit einem Text-Editor geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a2298-115">The files can be modified with a text editor.</span></span> <span data-ttu-id="a2298-116">Um die in den SPD-und Sad-Dateien enthaltene Konfiguration aufzurufen, verwenden Sie den Befehl **dem ipsec6 a** .</span><span class="sxs-lookup"><span data-stu-id="a2298-116">To invoke the configuration contained in the SPD and SAD files, use the **ipsec6 a** command.</span></span>

</dd> <dt>

<span data-ttu-id="a2298-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**dem ipsec6 a \[** _Dateiname (ohne Erweiterung)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="a2298-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 a \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a2298-118">Fügt der Liste der aktiven Sicherheitsrichtlinien und Sicherheits Zuordnungen Sicherheitsrichtlinien in *filename*. SPD und Sicherheits Zuordnungen in *filename*. Sad hinzu.</span><span class="sxs-lookup"><span data-stu-id="a2298-118">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations.</span></span>

</dd> <dt>

<span data-ttu-id="a2298-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**dem ipsec6 i \[**  *_Richtlinien \] \[_* _Dateiname (ohne Erweiterung)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="a2298-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[**_Policy_*_\] \[_*_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a2298-120">Fügt der Liste aktiver Sicherheitsrichtlinien und Sicherheits Zuordnungen, auf die durch die Richtlinien Nummer verwiesen wird, Sicherheitsrichtlinien in *filename*. SPD und Sicherheits Zuordnungen in *filename*. Sad hinzu.</span><span class="sxs-lookup"><span data-stu-id="a2298-120">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations as referenced by policy number.</span></span>

</dd> <dt>

<span data-ttu-id="a2298-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**dem ipsec6 d \[ Type = SP SA \] \[** _indexnumber_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="a2298-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[type = sp sa\] \[**_IndexNumber_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a2298-122">Löscht Sicherheitsrichtlinien oder Sicherheits Zuordnungen aus der Liste der aktiven Sicherheitsrichtlinien und Sicherheits Zuordnungen, wie von ihrer Indexnummer referenziert (angezeigt mit **dem ipsec6 sp** oder **dem ipsec6 SA**).</span><span class="sxs-lookup"><span data-stu-id="a2298-122">Deletes security policies or security associations from the list of active security policies and security associations, as referenced by their index number (displayed with **ipsec6 sp** or **ipsec6 sa**).</span></span>

</dd> </dl>

 

 



