---
description: Definiert ein Attribut eines Zählers, der angibt, wie die gegen Daten in einer Consumeranwendung angezeigt werden.
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: komplexer counterAttribute-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1b34a3a802f0f7c79815956c3a364522ce0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359043"
---
# <a name="counterattribute-complex-type"></a><span data-ttu-id="7a526-103">komplexer counterAttribute-Typ</span><span class="sxs-lookup"><span data-stu-id="7a526-103">counterAttribute Complex Type</span></span>

<span data-ttu-id="7a526-104">Definiert ein Attribut eines Zählers, der angibt, wie die gegen Daten in einer Consumeranwendung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7a526-104">Defines an attribute of a counter that specifies how the counter data is displayed in a consumer application.</span></span>

``` syntax
<xs:complexType name="counterAttribute">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                use="required"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="xs:string"
                    >
                        <xs:enumeration
                            value="reference"
                         />
                        <xs:enumeration
                            value="noDisplay"
                         />
                        <xs:enumeration
                            value="noDigitGrouping"
                         />
                        <xs:enumeration
                            value="displayAsHex"
                         />
                        <xs:enumeration
                            value="displayAsReal"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="7a526-105">Attributes</span><span class="sxs-lookup"><span data-stu-id="7a526-105">Attributes</span></span>



| <span data-ttu-id="7a526-106">Name</span><span class="sxs-lookup"><span data-stu-id="7a526-106">Name</span></span> | <span data-ttu-id="7a526-107">type</span><span class="sxs-lookup"><span data-stu-id="7a526-107">Type</span></span> | <span data-ttu-id="7a526-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a526-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a526-109">name</span><span class="sxs-lookup"><span data-stu-id="7a526-109">name</span></span> |      | <span data-ttu-id="7a526-110">Der Name des anzuwendenden Anzeige Attributs.</span><span class="sxs-lookup"><span data-stu-id="7a526-110">The name of the display attribute to apply.</span></span> <span data-ttu-id="7a526-111">Sie können einen der folgenden Namen angeben:</span><span class="sxs-lookup"><span data-stu-id="7a526-111">You can specify one of the following names:</span></span><br/> <dl> <span data-ttu-id="7a526-112"><dt><span id="reference"></span><span id="REFERENCE"></span>Referenz</dt></span><span class="sxs-lookup"><span data-stu-id="7a526-112"><dt><span id="reference"></span><span id="REFERENCE"></span>reference</dt></span></span> <dd> <span data-ttu-id="7a526-113">Rufen Sie den Wert des Zählers als Verweis und nicht als Wert ab.</span><span class="sxs-lookup"><span data-stu-id="7a526-113">Retrieve the value of the counter by reference as opposed to by value.</span></span><br/> </dd> <span data-ttu-id="7a526-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>nodisplay</dt></span><span class="sxs-lookup"><span data-stu-id="7a526-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>noDisplay</dt></span></span> <dd> <span data-ttu-id="7a526-115">Zeigen Sie den Wert des Leistungs Zählers nicht an.</span><span class="sxs-lookup"><span data-stu-id="7a526-115">Do not display the counter value.</span></span> <span data-ttu-id="7a526-116">In der Regel verwenden Sie dieses Attribut, wenn die Daten des Zählers als Eingabe zum Berechnen des Werts eines anderen Zählers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a526-116">Typically, you use this attribute if the counter's data is used as input for calculating another counter's value.</span></span> <br/> </dd> <span data-ttu-id="7a526-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>nodigit-Gruppierung</dt></span><span class="sxs-lookup"><span data-stu-id="7a526-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span></span> <dd> <span data-ttu-id="7a526-118">Consumer-oder Überwachungsanwendungen sollten keine Ziffern Trennzeichen verwenden, wenn Sie Zählerwerte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a526-118">Consumer or monitoring applications should not use digit separators when displaying counter values.</span></span> <br/> </dd> <span data-ttu-id="7a526-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>Display AshEx</dt></span><span class="sxs-lookup"><span data-stu-id="7a526-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span></span> <dd> <span data-ttu-id="7a526-120">Consumer-oder Überwachungsanwendungen sollten den Wert des Zählers als Hexadezimalwert anstelle der standardmäßigen Ganzzahl anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a526-120">Consumer or monitoring applications should display the counter value as a hexadecimal, instead of the default integer value.</span></span><br/> </dd> <span data-ttu-id="7a526-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayasreal</dt></span><span class="sxs-lookup"><span data-stu-id="7a526-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span></span> <dd> <span data-ttu-id="7a526-122">Consumer-oder Überwachungsanwendungen sollten den Wert des Zählers als reelle Zahl anstelle der standardmäßigen Ganzzahl anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a526-122">Consumer or monitoring applications should display the counter value as a real number, instead of the default integer value.</span></span> <br/> </dd> </dl> |



## <a name="requirements"></a><span data-ttu-id="7a526-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a526-123">Requirements</span></span>



| <span data-ttu-id="7a526-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a526-124">Requirement</span></span> | <span data-ttu-id="7a526-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7a526-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a526-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a526-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7a526-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a526-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7a526-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a526-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7a526-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a526-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




