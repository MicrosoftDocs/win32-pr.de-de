---
description: Sie können keine Instanzen der geänderten Klassen im lokalisierten Namespace erstellen. Geänderte Klassen im lokalisierten Namespace werden so behandelt, als wären Sie abstrakt, obwohl Sie nicht den abstrakten Qualifizierer enthalten.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Überlegungen zu geänderten Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218816"
---
# <a name="amended-class-considerations"></a><span data-ttu-id="b9dc9-104">Überlegungen zu geänderten Klassen</span><span class="sxs-lookup"><span data-stu-id="b9dc9-104">Amended Class Considerations</span></span>

<span data-ttu-id="b9dc9-105">Sie können keine Instanzen der geänderten Klassen im lokalisierten Namespace erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9dc9-105">You cannot create instances of the amended classes in the localized namespace.</span></span> <span data-ttu-id="b9dc9-106">Geänderte Klassen im lokalisierten Namespace werden so behandelt, als wären Sie abstrakt, obwohl Sie nicht den [**abstrakten**](standard-qualifiers.md) Qualifizierer enthalten.</span><span class="sxs-lookup"><span data-stu-id="b9dc9-106">Amended classes in the localized namespace are treated as if they are abstract although they do not contain the [**Abstract**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="b9dc9-107">Wenn Sie mit dem WBEM-Flag eine geänderte Klasse aus einem lokalisierten Namespace abrufen, indem Sie das \_ \_ Flag "geänderte Qualifizierer" verwenden \_ \_ und eine Instanz daraus erzeugen, enthält die Instanz alle geänderten Qualifizierer der geänderten Klasse.</span><span class="sxs-lookup"><span data-stu-id="b9dc9-107">If you retrieve an amended class from a localized namespace using the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag and spawn an instance from it, the instance contains all of the amended qualifiers of the amended class.</span></span> <span data-ttu-id="b9dc9-108">Diese neue Klasse kann nicht im-Namespace gespeichert werden, der die grundlegende Klassendefinition enthält, es sei denn, Sie führen den **Put** -Vorgang mit dem WBEM- \_ Flag \_ Verwenden der \_ geänderten \_ qualifiziererflag</span><span class="sxs-lookup"><span data-stu-id="b9dc9-108">You cannot store this new class in the namespace that contains the basic class definition unless you perform the **put** operation with the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span> <span data-ttu-id="b9dc9-109">Dieses Flag weist WMI an, alle geänderten Qualifizierer zu entfernen, bevor das Objekt gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="b9dc9-109">This flag instructs WMI to strip away any amended qualifiers before saving the object.</span></span> <span data-ttu-id="b9dc9-110">Wenn Sie das WBEM-Flag nicht für \_ \_ \_ die Verwendung \_ von geänderten Qualifizierern angeben, schlägt der **Put** -Vorgang mit einem WBEM \_ E- \_ \_ Objekt Fehler fehl.</span><span class="sxs-lookup"><span data-stu-id="b9dc9-110">If you do not specify WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS, the **put** operation fails with a WBEM\_E\_AMENDED\_OBJECT error.</span></span>

 

 



