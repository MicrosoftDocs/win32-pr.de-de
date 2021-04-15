---
title: komplexer exectype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen des exec (aktiongroup)-Elements.
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- komplexer exectype-Typ Taskplaner
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475651"
---
# <a name="exectype-complex-type"></a><span data-ttu-id="9c567-104">komplexer exectype-Typ</span><span class="sxs-lookup"><span data-stu-id="9c567-104">execType Complex Type</span></span>

<span data-ttu-id="9c567-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen des [**exec (aktiongroup)**](taskschedulerschema-exec-actiongroup-element.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="9c567-105">Defines the child elements and sequencing information of the [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9c567-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9c567-106">Child elements</span></span>



| <span data-ttu-id="9c567-107">Element</span><span class="sxs-lookup"><span data-stu-id="9c567-107">Element</span></span>                                                                           | <span data-ttu-id="9c567-108">type</span><span class="sxs-lookup"><span data-stu-id="9c567-108">Type</span></span>                                                        | <span data-ttu-id="9c567-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c567-109">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c567-110">**Argumente**</span><span class="sxs-lookup"><span data-stu-id="9c567-110">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="9c567-111">**string**</span><span class="sxs-lookup"><span data-stu-id="9c567-111">**string**</span></span>                                                  | <span data-ttu-id="9c567-112">Gibt die Argumente an, die dem Befehlszeilen Vorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9c567-112">Specifies the arguments associated with the command-line operation.</span></span> <br/>                              |
| [<span data-ttu-id="9c567-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="9c567-113">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | [<span data-ttu-id="9c567-114">**PathType**</span><span class="sxs-lookup"><span data-stu-id="9c567-114">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="9c567-115">Gibt die ausführbare Datei oder das Dokument an, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c567-115">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="9c567-116">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="9c567-116">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | [<span data-ttu-id="9c567-117">**PathType**</span><span class="sxs-lookup"><span data-stu-id="9c567-117">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="9c567-118">Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9c567-118">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9c567-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c567-119">Requirements</span></span>



| <span data-ttu-id="9c567-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c567-120">Requirement</span></span> | <span data-ttu-id="9c567-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9c567-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c567-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c567-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9c567-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c567-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c567-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c567-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9c567-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c567-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c567-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c567-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c567-127">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="9c567-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="9c567-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="9c567-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





