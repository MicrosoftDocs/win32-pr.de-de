---
title: Integrieren von Schema Erweiterungen in die Benutzeroberfläche
description: Die Verwaltungs Tools von Active Directory Domain Services verwenden eine gängige Architektur zum Verbinden der administrativen Benutzeroberfläche mit dem Verzeichnisschema.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337961"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a><span data-ttu-id="7170c-103">Integrieren von Schema Erweiterungen in die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="7170c-103">Integrating Schema Extensions with the User Interface</span></span>

<span data-ttu-id="7170c-104">Die Verwaltungs Tools von Active Directory Domain Services verwenden eine gängige Architektur zum Verbinden der administrativen Benutzeroberfläche mit dem Verzeichnisschema.</span><span class="sxs-lookup"><span data-stu-id="7170c-104">The administration tools of Active Directory Domain Services use a common architecture for connecting the administrative user interface to the directory schema.</span></span> <span data-ttu-id="7170c-105">Das Kernstück dieser Architektur ist die **displaySpecifier** -Objektklasse.</span><span class="sxs-lookup"><span data-stu-id="7170c-105">The centerpiece of this architecture is the **displaySpecifier** object class.</span></span> <span data-ttu-id="7170c-106">Anzeige spezifier und deren Verwendung werden ausführlich unter [Erweitern der Benutzeroberfläche für Verzeichnisobjekte](extending-the-user-interface-for-directory-objects.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7170c-106">Display specifiers and their usage are described in detail in [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

<span data-ttu-id="7170c-107">Wenn Sie eine neue Klasse erstellen, indem Sie eine Unterklasse einer vorhandenen Klasse erstellen, können Sie die vorhandene Benutzeroberfläche für die übergeordnete Klasse nutzen, indem Sie den Anzeigespezifizierer der übergeordneten Klasse kopieren.</span><span class="sxs-lookup"><span data-stu-id="7170c-107">When you create a new class by subclassing an existing class, you can leverage the existing UI for the superclass by copying the superclass' display specifier.</span></span> <span data-ttu-id="7170c-108">Eine einfache Möglichkeit, den Anzeige Spezifizierer für eine Klasse zu kopieren, besteht darin, Sie mithilfe von LDIFDE in eine LDIF-Datei zu exportieren, den Distinguished Name und den CN zu bearbeiten und dann die geänderte LDIF-Datei zu importieren.</span><span class="sxs-lookup"><span data-stu-id="7170c-108">An easy way to copy the display specifier for a class is to export it into an LDIF file using LDIFDE, edit the Distinguished name and CN, then import the modified LDIF file.</span></span> <span data-ttu-id="7170c-109">Wenn die Unterklasse über zusätzliche Attribute verfügt, müssen Sie zusätzliche Eigenschaften Seiten bereitstellen, um die Bearbeitung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7170c-109">If the subclass has additional attributes, you will need to provide additional property pages to support editing.</span></span> <span data-ttu-id="7170c-110">Wenn die Unterklasse über zusätzliche erforderliche Eigenschaften verfügt, müssen Sie Erweiterungs Seiten für das Erstellen von Dialog Feld bereitstellen, da die von der übergeordneten Klasse bereitgestellte Benutzeroberfläche keine Möglichkeit zum Erstellen dieser neuen Attribute hat.</span><span class="sxs-lookup"><span data-stu-id="7170c-110">If the subclass has additional must-have properties, you will need to provide Creation Dialog extension pages since the UI provided by the superclass has no way to create these new attributes.</span></span>

 

 




