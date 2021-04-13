---
description: Sie können Registrierungsschlüssel in die Systemregistrierung schreiben, nachdem alle ausgewählten Komponenten und die zugehörigen Dateien installiert wurden.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Ändern der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348528"
---
# <a name="modifying-the-registry"></a><span data-ttu-id="d500d-103">Ändern der Registrierung</span><span class="sxs-lookup"><span data-stu-id="d500d-103">Modifying the Registry</span></span>

<span data-ttu-id="d500d-104">Sie können Registrierungsschlüssel in die Systemregistrierung schreiben, nachdem alle ausgewählten Komponenten und die zugehörigen Dateien installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d500d-104">Registry keys can be written to the system registry once all selected components and their related files have been installed.</span></span> <span data-ttu-id="d500d-105">Die Standard Aktionen im Zusammenhang mit der Änderung der Registrierung müssen nach den Standard Aktionen für die Datei Installation sequenziert werden, da Registrierungsschlüssel nicht geschrieben werden können, es sei denn, die entsprechende Komponente und Datei wurde erfolgreich installiert.</span><span class="sxs-lookup"><span data-stu-id="d500d-105">The standard actions related to modifying the registry must be sequenced after the file installation standard actions because registry keys cannot be written unless the corresponding component and file have been successfully installed.</span></span>

<span data-ttu-id="d500d-106">Die [RegisterClassInfo-Aktion](registerclassinfo-action.md) greift auf die [Klassen Tabelle](class-table.md) zu, um die com-Klassen Informationen der installierten Komponenten zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d500d-106">The [RegisterClassInfo action](registerclassinfo-action.md) accesses the [Class table](class-table.md) to register the COM class information of the installed components.</span></span>

<span data-ttu-id="d500d-107">Mit der [RegisterExtensionInfo-Aktion](registerextensioninfo-action.md) werden die [Erweiterungs Tabelle](extension-table.md) und die [Verb Tabelle](verb-table.md) abgefragt, und die entsprechenden Erweiterungen und Befehls-Verb-Informationen werden mit dem Betriebssystem registriert.</span><span class="sxs-lookup"><span data-stu-id="d500d-107">The [RegisterExtensionInfo action](registerextensioninfo-action.md) queries the [Extension table](extension-table.md) and [Verb table](verb-table.md) and registers the corresponding extensions and command-verb information with the operating system.</span></span>

<span data-ttu-id="d500d-108">Mit der [registerprogidinfo-Aktion](registerprogidinfo-action.md) wird die Registrierung von OLE-ProgID-Informationen beim Betriebssystem verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d500d-108">The [RegisterProgIdInfo action](registerprogidinfo-action.md) manages the registration of OLE ProgId information with the operating system.</span></span>

<span data-ttu-id="d500d-109">Die [registermimeinfo-Aktion](registermimeinfo-action.md) verarbeitet die [MIME-Tabelle](mime-table.md) , um die Zuordnung zwischen einem MIME-Kontexttyp, der Dateinamenerweiterung und der CLSID zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d500d-109">The [RegisterMIMEInfo action](registermimeinfo-action.md) processes the [MIME table](mime-table.md) to register the association between a MIME context type, the file name extension, and the CLSID.</span></span>

<span data-ttu-id="d500d-110">Die [Aktion "beschreiteregistryvalues](writeregistryvalues-action.md) " verarbeitet die [Registrierungs Tabelle](registry-table.md) und schreibt die Schlüssel für alle Komponenten, die entweder lokal oder aus der Quelle installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d500d-110">The [WriteRegistryValues action](writeregistryvalues-action.md) processes the [Registry table](registry-table.md) and writes the keys for all components that have been either installed locally or to run from source.</span></span> <span data-ttu-id="d500d-111">In der Registrierungs Tabelle können Schlüssel in die Registrierungs Strukturen der **HKEY- \_ Klassen \_ root**, **HKEY \_ Current \_ User**, **HKEY \_ local \_ Machine** und **HKEY \_ Users** geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d500d-111">The Registry table allows keys to be written to the **HKEY\_CLASSES\_ROOT**, **HKEY\_CURRENT\_USER**, **HKEY\_LOCAL\_MACHINE**, and **HKEY\_USERS** registry hives.</span></span>

<span data-ttu-id="d500d-112">Mit der [Aktion removeregistryvalues](removeregistryvalues-action.md) werden die Schlüssel, die zum Löschen markiert wurden, in der Spalte Name der [Registrierungs Tabelle](registry-table.md) oder der [Tabelle removeregistry](removeregistry-table.md)entfernt.</span><span class="sxs-lookup"><span data-stu-id="d500d-112">The [RemoveRegistryValues action](removeregistryvalues-action.md) removes the keys that have been marked to be deleted in the Name column of the [Registry table](registry-table.md) or the [RemoveRegistry Table](removeregistry-table.md).</span></span>

<span data-ttu-id="d500d-113">Die [Aktion registertypelibraries](registertypelibraries-action.md) verarbeitet die [typelib-Tabelle](typelib-table.md) und registriert die installierten Typbibliotheken beim System.</span><span class="sxs-lookup"><span data-stu-id="d500d-113">The [RegisterTypeLibraries action](registertypelibraries-action.md) processes the [TypeLib table](typelib-table.md) and registers the installed type libraries with the system.</span></span>

 

 



