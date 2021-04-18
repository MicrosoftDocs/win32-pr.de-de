---
description: ICE53 prüft Einträge in der Registrierungs Tabelle, die Informationen zum privaten Installer oder Richtlinien Werte in die Systemregistrierung schreiben.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350798"
---
# <a name="ice53"></a><span data-ttu-id="d1c67-103">ICE53</span><span class="sxs-lookup"><span data-stu-id="d1c67-103">ICE53</span></span>

<span data-ttu-id="d1c67-104">ICE53 prüft Einträge in der Registrierungs Tabelle, die Informationen zum privaten Installer oder Richtlinien Werte in die Systemregistrierung schreiben.</span><span class="sxs-lookup"><span data-stu-id="d1c67-104">ICE53 checks for entries in the Registry table that write private installer information or policy values to the system registry.</span></span>

## <a name="result"></a><span data-ttu-id="d1c67-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="d1c67-105">Result</span></span>

<span data-ttu-id="d1c67-106">ICE53 gibt eine Warnung aus, wenn in der Registrierungs Tabelle das Schreiben interner oder Richtlinien Informationen in die Registrierung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d1c67-106">ICE53 posts a warning if the Registry table specifies writing internal or policy information to the registry.</span></span>

## <a name="example"></a><span data-ttu-id="d1c67-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d1c67-107">Example</span></span>

<span data-ttu-id="d1c67-108">ICE53 gibt die folgende Warnung für das gezeigte Beispiel aus.</span><span class="sxs-lookup"><span data-stu-id="d1c67-108">ICE53 posts the following warning for the example shown.</span></span>

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

<span data-ttu-id="d1c67-109">[Registrierungs Tabelle](registry-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d1c67-109">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="d1c67-110">Registrierung</span><span class="sxs-lookup"><span data-stu-id="d1c67-110">Registry</span></span>             | <span data-ttu-id="d1c67-111">Root</span><span class="sxs-lookup"><span data-stu-id="d1c67-111">Root</span></span>         | <span data-ttu-id="d1c67-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d1c67-112">Key</span></span>                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c67-113">Registry1</span><span class="sxs-lookup"><span data-stu-id="d1c67-113">Registry1</span></span><br/> | <span data-ttu-id="d1c67-114">1</span><span class="sxs-lookup"><span data-stu-id="d1c67-114">1</span></span><br/> | <span data-ttu-id="d1c67-115">**Software** \\ **Richtlinien** \\ **Microsoft** \\ **Windows** \\ **Installer** \\ **DISABLEROLLBACK**</span><span class="sxs-lookup"><span data-stu-id="d1c67-115">**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**DisableRollback**</span></span><br/> |



 

<span data-ttu-id="d1c67-116">In der Registrierungs Tabellenzeile "Registry1" wird ein Systemrichtlinien Wert in die Registrierung geschrieben, der sich auf die Installation aller Pakete auswirkt.</span><span class="sxs-lookup"><span data-stu-id="d1c67-116">Registry table row 'Registry1' writes a system policy value in the registry that affects the installation of all packages.</span></span> <span data-ttu-id="d1c67-117">Abhängig vom Paket kann es möglich sein, das Rollback für dieses Paket allein zu deaktivieren, indem die [**DISABLEROLLBACK**](-disablerollback.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d1c67-117">Depending on the package, it may be possible to disable rollback for this package alone by setting the [**DISABLEROLLBACK**](-disablerollback.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="d1c67-118">Siehe [Rollback-Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="d1c67-118">See [Rollback Installation](rollback-installation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1c67-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1c67-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1c67-120">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="d1c67-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




