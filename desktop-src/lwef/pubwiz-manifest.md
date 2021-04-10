---
title: Verwenden des Übertragungs Manifests
description: Der Webpublishing-Assistent und der Assistent für die Online druckbestellung verwenden das Übertragungs Manifest, um Details der Datenübertragung zwischen dem Client Computer und dem Serverstandort zu kommunizieren.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Webpublishing-Assistent, übertragen des Manifests
- Online-druckstellungs-Assistent, übertragen des Manifests
- Übertragungs Manifest
- manifest
- Window. extern, Übertragungs Manifest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858245"
---
# <a name="using-the-transfer-manifest"></a><span data-ttu-id="f0c73-108">Verwenden des Übertragungs Manifests</span><span class="sxs-lookup"><span data-stu-id="f0c73-108">Using the Transfer Manifest</span></span>

<span data-ttu-id="f0c73-109">Der Webpublishing-Assistent und der Assistent für die Online druckbestellung verwenden das Übertragungs Manifest, um Details der Datenübertragung zwischen dem Client Computer und dem Serverstandort zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f0c73-109">The Web Publishing Wizard and Online Print Ordering Wizard use the transfer manifest to communicate details of data transfer between the client computer and the server site.</span></span>

## <a name="the-purpose-of-the-transfer-manifest"></a><span data-ttu-id="f0c73-110">Der Zweck des Übertragungs Manifests.</span><span class="sxs-lookup"><span data-stu-id="f0c73-110">The Purpose of the Transfer Manifest</span></span>

<span data-ttu-id="f0c73-111">Das Übertragungs Manifest beschreibt die an der Übertragung beteiligten Dateien, einschließlich Details wie der Ziel Hierarchie und den Metadaten der Datei.</span><span class="sxs-lookup"><span data-stu-id="f0c73-111">The transfer manifest describes files involved in the transfer, including details such as the destination hierarchy and the file's metadata.</span></span> <span data-ttu-id="f0c73-112">Das Manifest kann durch ein Server seitiges Skript geändert werden, indem ungeeignete Dateien aus der Liste entfernt werden und Informationen darüber hinzugefügt werden, wie und wo die Dateien übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0c73-112">Server-side script can modify the manifest by removing inappropriate files from the list and adding information about how and where the files should be transferred.</span></span>

<span data-ttu-id="f0c73-113">Das Manifest wird als Eigenschaften **Fenster. extern. Property ("transfermanifest")**, ein XML-Dokumentobjektmodell Dokument (DOM) verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="f0c73-113">The manifest is exposed as the property **window.external.Property("TransferManifest")**, an XML Document Object Model (DOM) document.</span></span> <span data-ttu-id="f0c73-114">Weitere Informationen zum XML-DOM finden Sie in der MSDN-Dokumentation zu [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0c73-114">For more information on the XML DOM, see the MSDN documentation for [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span></span>

<span data-ttu-id="f0c73-115">Die Organisation der obersten Ebene des Übertragungs Manifests lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f0c73-115">The top-level organization of the transfer manifest is as follows:</span></span>


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



<span data-ttu-id="f0c73-116">Die serverseitige HTML-Seite kann mithilfe der Knoten im Manifest bestimmte Informationen zu den zu kopierenden Dateien abrufen und dann die Benutzeroberfläche des dienstanders entsprechend ändern.</span><span class="sxs-lookup"><span data-stu-id="f0c73-116">The server-side HTML page can use the nodes in the manifest to obtain certain information about the files to be copied and then modify the service's UI accordingly.</span></span> <span data-ttu-id="f0c73-117">Beispielsweise kann eine Foto Druck Site die Informationen verwenden, um Miniaturansichten der ausgewählten Images anzuzeigen, während ein Speicherort die Informationen verwenden könnte, um sicherzustellen, dass ausreichend Speicherplatz für diesen Benutzer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f0c73-117">For instance, a photo printing site might use the information to display thumbnails of the chosen images, while a storage site might use the information to ensure that sufficient storage space is available for that user.</span></span> <span data-ttu-id="f0c73-118">Umfassende Informationen zu den Knoten und Attributen für das Übertragen von Manifests finden Sie unter [übertragen des manifest-Schemas](/windows/desktop/shell/interfaces)</span><span class="sxs-lookup"><span data-stu-id="f0c73-118">For complete information on the transfer manifest nodes and attributes, see [Transfer Manifest Schema](/windows/desktop/shell/interfaces).</span></span>

<span data-ttu-id="f0c73-119">Das Schema des Übertragungs Manifests wird als offenes Modell geschrieben, sodass Elemente, die nicht speziell im Schema definiert sind, im Übertragungs Manifest angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="f0c73-119">The transfer manifest schema is written as an open model so that elements not specifically defined in the schema may appear in the transfer manifest.</span></span> <span data-ttu-id="f0c73-120">Daher kann eine Anbieter Site proprietäre Elemente zur eigenen Verwendung hinzufügen, ohne die Gültigkeit des Manifests zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="f0c73-120">Therefore, a provider site might add proprietary elements for its own use without disturbing the validity of the manifest.</span></span> <span data-ttu-id="f0c73-121">Das Schema ist auch so definiert, dass die Reihenfolge der Elemente nicht eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="f0c73-121">The schema is also defined so that the order of elements is not restricted.</span></span>

> [!Note]  
> <span data-ttu-id="f0c73-122">Das Manifest wird jedes Mal neu erstellt, wenn ein neuer Anbieter ausgewählt wird, damit der Anbieter die Möglichkeit hat, Site Informationen im Manifest zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f0c73-122">The manifest is re-created each time a new provider is chosen so that the provider has a chance to store site information in the manifest.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f0c73-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0c73-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0c73-124">Schema des Übertragungs Manifests</span><span class="sxs-lookup"><span data-stu-id="f0c73-124">Transfer Manifest Schema</span></span>](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 