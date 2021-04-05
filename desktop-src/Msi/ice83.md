---
description: ICE83 überprüft die MsiAssembly-Tabelle.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042147"
---
# <a name="ice83"></a><span data-ttu-id="37666-103">ICE83</span><span class="sxs-lookup"><span data-stu-id="37666-103">ICE83</span></span>

<span data-ttu-id="37666-104">ICE83 überprüft die [MsiAssembly-Tabelle](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="37666-104">ICE83 validates the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="37666-105">Diese benutzerdefinierte Ice-Aktion sendet einen Fehler, wenn der Schlüssel Pfad für eine Komponente, die eine Win32-Assembly enthält, auf die Manifest-Datei festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="37666-105">This ICE custom action posts an error if the key path for a component containing a Win32 assembly is set to the manifest file.</span></span> <span data-ttu-id="37666-106">Der Fehler wird explizit ausgegeben, wenn der im KEYPATH-Feld der [Komponenten Tabelle](component-table.md) eingegebene Wert gleich dem Wert ist, der im Feld "Datei \_ Manifest" der Tabelle "MsiAssembly" eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="37666-106">Explicitly the error is posted if the value entered in the KeyPath field of the [Component table](component-table.md) equals the value entered in the File\_Manifest field of the MsiAssembly table.</span></span> <span data-ttu-id="37666-107">Diese benutzerdefinierte Ice-Aktion gibt einen Fehler aus, wenn mindestens ein Datensatz in der MsiAssembly-Tabelle vorhanden ist und die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) nicht sowohl die [msipublishassemblierungsaktion](msipublishassemblies-action.md) als auch die [msiunpublishassemblyaktion](msiunpublishassemblies-action.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="37666-107">This ICE custom action posts an error if there is at least one record in the MsiAssembly table and the [InstallExecuteSequence table](installexecutesequence-table.md) does not contain both the [MsiPublishAssemblies Action](msipublishassemblies-action.md) and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

## <a name="result"></a><span data-ttu-id="37666-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="37666-108">Result</span></span>

<span data-ttu-id="37666-109">ICE83 gibt die folgenden Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="37666-109">ICE83 posts the following errors.</span></span>



| <span data-ttu-id="37666-110">ICE83-Fehler</span><span class="sxs-lookup"><span data-stu-id="37666-110">ICE83 error</span></span>                                                                                                   | <span data-ttu-id="37666-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37666-111">Description</span></span>                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37666-112">Der Schlüssel Pfad für die Win32-SxS-Assembly (Komponente \_ = \[ 1 \] ) sollte nicht die Manifest-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="37666-112">The key path for Win32 SXS Assembly (Component\_=\[1\]) SHOULD NOT be its manifest file</span></span>                       | <span data-ttu-id="37666-113">ICE83 gibt diesen Fehler aus, wenn das KEYPATH-Feld für eine Win32-Assembly auf die zugehörige Manifest-Datei (Component. KEYPATH = = MsiAssembly. File Manifest) festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="37666-113">ICE83 posts this error when the KeyPath field for a Win32 Assembly is set to its manifest file (Component.KeyPath == MsiAssembly.File\_Manifest).</span></span> <span data-ttu-id="37666-114">\[1 \] ist ein KEYPATH in der Component-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="37666-114">\[1\] is KeyPath in Component table</span></span>                          |
| <span data-ttu-id="37666-115">In der InstallExecuteSequence-Tabelle müssen sowohl msipublishassemblys als auch msiunpublishassemblyaktionen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="37666-115">Both MsiPublishAssemblies AND MsiUnpublishAssemblies actions MUST be present in InstallExecuteSequence table.</span></span> | <span data-ttu-id="37666-116">ICE83 gibt diesen Fehler aus, wenn mindestens ein Eintrag in der MsiAssembly-Tabelle vorhanden ist, aber die InstallExecuteSequence-Tabelle nicht gleichzeitig die msiassemblypublish-Aktion und die msiassemblyunpublish-Aktion enthält.</span><span class="sxs-lookup"><span data-stu-id="37666-116">ICE83 posts this error when there is at least one entry in the MsiAssembly table but the InstallExecuteSequence table does not contain both the MsiAssemblyPublish action and the MsiAssemblyUnpublish action.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="37666-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37666-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37666-118">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="37666-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



