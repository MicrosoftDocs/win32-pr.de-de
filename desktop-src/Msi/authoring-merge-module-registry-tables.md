---
description: Verwenden Sie die Merge Module-Registrierungs Tabellen gemäß dem Typ der Registrierungsinformationen.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Erstellen von Mergemodul-Registrierungs Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959515"
---
# <a name="authoring-merge-module-registry-tables"></a><span data-ttu-id="9233b-103">Erstellen von Mergemodul-Registrierungs Tabellen</span><span class="sxs-lookup"><span data-stu-id="9233b-103">Authoring Merge Module Registry Tables</span></span>

<span data-ttu-id="9233b-104">Verwenden Sie die Merge Module-Registrierungs Tabellen gemäß dem Typ der Registrierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="9233b-104">Use Merge Module Registry tables according to the type of registry information.</span></span>

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a><span data-ttu-id="9233b-105">TypeLib, Class, AppID, ProgID, Extension, Verb oder MIME-Tabellen</span><span class="sxs-lookup"><span data-stu-id="9233b-105">TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME Tables</span></span>

<span data-ttu-id="9233b-106">Für Typbibliotheken, Klassen, Erweiterungen und Verben erstellen Sie Registrierungsinformationen in den Tabellen [typelib](typelib-table.md), [Klasse](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)oder [MIME](mime-table.md) des Mergemoduls.</span><span class="sxs-lookup"><span data-stu-id="9233b-106">For type libraries, classes, extensions, and verbs, author registry information into the merge module's [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="9233b-107">Wenn Sie die [Registrierungs Tabelle](registry-table.md) zum Hinzufügen dieser Informationen verwenden, kann Windows 2000 keine systemweiten Ankündigungen für diese Komponenten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9233b-107">If you use the [Registry table](registry-table.md) to add this information, Windows 2000 cannot provide system-wide advertisement for these components.</span></span>

<span data-ttu-id="9233b-108">Autoren von Mergemodulen können sich aus den folgenden Gründen entscheiden, sich nicht mithilfe der Klassen Tabelle zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="9233b-108">Merge module authors may decide not to register using the Class table for the following reasons:</span></span>

-   <span data-ttu-id="9233b-109">Um von der Klassen Tabelle registriert zu werden, muss es sich bei der Datei um den KEYPATH der zugehörigen Komponente handeln.</span><span class="sxs-lookup"><span data-stu-id="9233b-109">To be registered by the Class table, the file has to be the KeyPath of its component.</span></span> <span data-ttu-id="9233b-110">Dies erfordert möglicherweise eine akzeptable Änderung in der Organisation der Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9233b-110">This may require an unacceptable change in the organization of components.</span></span>
-   <span data-ttu-id="9233b-111">Ein com-Befehl löst möglicherweise einen Installationsversuch aus, eine angekündigte Klasse erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9233b-111">A COM call may trigger an installer attempt to reinstall an advertised class.</span></span> <span data-ttu-id="9233b-112">Autoren können sich entscheiden, eine Klasse nicht mithilfe der Klassen Tabelle zu registrieren, um zu vermeiden, dass eine Neuinstallation ausgelöst wird, wenn der Client Computer eine Benutzeroberfläche nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9233b-112">Authors may decide not to register a class using the Class table in order to avoid triggering a reinstallation when the client computer does not support a user interface.</span></span>

## <a name="registry-table"></a><span data-ttu-id="9233b-113">Registrierungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="9233b-113">Registry Table</span></span>

<span data-ttu-id="9233b-114">Verwenden Sie die Registrierungs Tabelle, um Registrierungsinformationen hinzuzufügen, die nicht in den Tabellen TypeLib, Klasse, AppID, ProgID, Extension, Verb oder MIME erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="9233b-114">Use the Registry table to add registry information that cannot be authored into the TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME tables.</span></span> <span data-ttu-id="9233b-115">Windows 2000 kann keine systemweite Ankündigung für Komponenten bereitstellen, die die Registrierungs Tabelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="9233b-115">Windows 2000 cannot provide system-wide advertisement for components that use the Registry table.</span></span>

<span data-ttu-id="9233b-116">Wenn Sie die Registrierungs Tabelle erstellen, finden Sie weitere Informationen unter Dateipfade mithilfe der \[ \# Datei \] \[ . Datei \] Format anstelle von \[ Verzeichnis \] Dateiname.</span><span class="sxs-lookup"><span data-stu-id="9233b-116">When authoring the Registry table, refer to file paths using the \[\#File\] or \[!File\] format rather than as \[Directory\]Filename.</span></span> <span data-ttu-id="9233b-117">Das letztere Format unterstützt keine Installation von "Run-From-Source".</span><span class="sxs-lookup"><span data-stu-id="9233b-117">The latter format does not support run-from-source installation.</span></span> <span data-ttu-id="9233b-118">Im ersten Format werden fehlende Dateien und fehlerhafte Komponenten leichter erkannt.</span><span class="sxs-lookup"><span data-stu-id="9233b-118">The former format also makes missing files and faulty components easier to detect.</span></span>

<span data-ttu-id="9233b-119">Bei der Verwendung von formatiertem Text in der Schlüssel Spalte der Registrierungs Tabelle ist Vorsicht geboten.</span><span class="sxs-lookup"><span data-stu-id="9233b-119">Care is needed when using formatted text in the Key column of the Registry table.</span></span> <span data-ttu-id="9233b-120">Da Windows Installer keine Komponenten neu installiert, die bereits installiert sind, kann die Verwendung von formatiertem Text in diesem Feld dazu führen, dass Registrierungsschlüssel beim Entfernen der Anwendung zurückgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="9233b-120">Because Windows Installer does not reinstall components that are already installed, using formatted text in this field may cause registry keys to be left behind on application removal.</span></span>

## <a name="selfreg-table"></a><span data-ttu-id="9233b-121">Selfreg-Tabelle</span><span class="sxs-lookup"><span data-stu-id="9233b-121">SelfReg Table</span></span>

<span data-ttu-id="9233b-122">Die Verwendung der Tabelle "selfreg" wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9233b-122">Using the SelfReg table is not recommended.</span></span> <span data-ttu-id="9233b-123">Eine Liste der Gründe für die Verwendung der Selbstregistrierung finden Sie unter [selfreg Table](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="9233b-123">For a list of reasons for not using self-registration, see [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="9233b-124">Sie sollten stattdessen die Tabellen TypeLib, Klasse, AppID, ProgID, Extension, Verb und MIME verwenden, sofern möglich, und die Registrierungs Tabelle in allen anderen Fällen.</span><span class="sxs-lookup"><span data-stu-id="9233b-124">You should use the TypeLib, Class, AppId, ProgId, Extension, Verb, and MIME tables where possible instead and the Registry table in all other cases.</span></span>

 

 



