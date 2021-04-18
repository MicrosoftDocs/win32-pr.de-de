---
description: Die ColumnInfo-Eigenschaft des View-Objekts gibt ein Datensatz-Objekt zurück, das die angeforderten Informationen zu jeder Spalte im Resultset enthält.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: View. ColumnInfo-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364915"
---
# <a name="viewcolumninfo-property"></a><span data-ttu-id="f3d72-103">View. ColumnInfo-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f3d72-103">View.ColumnInfo property</span></span>

<span data-ttu-id="f3d72-104">Die **ColumnInfo** -Eigenschaft des [**View**](view-object.md) -Objekts gibt ein [**Datensatz**](record-object.md) -Objekt zurück, das die angeforderten Informationen zu jeder Spalte im Resultset enthält.</span><span class="sxs-lookup"><span data-stu-id="f3d72-104">The **ColumnInfo** property of the [**View**](view-object.md) object returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span> <span data-ttu-id="f3d72-105">Es können entweder die Spaltennamen oder die Spaltendefinitionen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f3d72-105">Either the column names or the column definitions may be requested.</span></span> <span data-ttu-id="f3d72-106">Die in der Auswahlliste angegebenen Konstanten haben keine Namen.</span><span class="sxs-lookup"><span data-stu-id="f3d72-106">Constants supplied in the Select list do not have names.</span></span>

<span data-ttu-id="f3d72-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f3d72-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d72-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3d72-108">Syntax</span></span>


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a><span data-ttu-id="f3d72-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f3d72-109">Property value</span></span>

<span data-ttu-id="f3d72-110">Erforderliche Informationen, die für jede Spalte benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="f3d72-110">Required information needed for each column.</span></span>



| <span data-ttu-id="f3d72-111">Parametername</span><span class="sxs-lookup"><span data-stu-id="f3d72-111">Parameter name</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="f3d72-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f3d72-112">Meaning</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <span data-ttu-id="f3d72-113"><dt>**msicolumninfonames**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3d72-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f3d72-114">Gibt die Namen aller nicht konstanten Spalten im Resultset zurück.</span><span class="sxs-lookup"><span data-stu-id="f3d72-114">Returns the names of all nonconstant columns in result set.</span></span><br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <span data-ttu-id="f3d72-115"><dt>**msicolumninfotypes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f3d72-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="f3d72-116">Gibt die Typen aller nicht konstanten Spalten im Resultset zurück.</span><span class="sxs-lookup"><span data-stu-id="f3d72-116">Returns the types of all nonconstant columns in result set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f3d72-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3d72-117">Remarks</span></span>

<span data-ttu-id="f3d72-118">Die von der **ColumnInfo** -Eigenschaft zurückgegebenen Spalten Beschreibungen weisen das Format auf, das im [Spalten Definitions Format](column-definition-format.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f3d72-118">The column descriptions returned by the **ColumnInfo** property are in the format described in [Column Definition Format](column-definition-format.md).</span></span> <span data-ttu-id="f3d72-119">Jede Spalte wird durch eine Zeichenfolge im entsprechenden Daten Satz Feld beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f3d72-119">Each column is described by a string in the corresponding record field.</span></span> <span data-ttu-id="f3d72-120">Die Definitions Zeichenfolge besteht aus einem einzelnen Buchstaben, der den Datentyp gefolgt von der Breite der Spalte darstellt (in Zeichen, falls zutreffend, oder else Bytes).</span><span class="sxs-lookup"><span data-stu-id="f3d72-120">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, or else bytes).</span></span> <span data-ttu-id="f3d72-121">Eine Breite von 0 (null) gibt eine unbegrenzte Breite an (lange Textfelder und Streams).</span><span class="sxs-lookup"><span data-stu-id="f3d72-121">A width of zero designates an unbounded width (long text fields and streams).</span></span> <span data-ttu-id="f3d72-122">Ein Großbuchstabe gibt an, dass NULL-Werte in der Spalte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f3d72-122">An uppercase letter indicates that Null values are allowed in the column.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d72-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3d72-123">Requirements</span></span>



| <span data-ttu-id="f3d72-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3d72-124">Requirement</span></span> | <span data-ttu-id="f3d72-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f3d72-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d72-126">Version</span><span class="sxs-lookup"><span data-stu-id="f3d72-126">Version</span></span><br/> | <span data-ttu-id="f3d72-127">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f3d72-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f3d72-128">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f3d72-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f3d72-129">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="f3d72-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f3d72-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f3d72-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="f3d72-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3d72-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f3d72-132">IID</span><span class="sxs-lookup"><span data-stu-id="f3d72-132">IID</span></span><br/>     | <span data-ttu-id="f3d72-133">IID \_ iView ist definiert als 000c109c-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f3d72-133">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




