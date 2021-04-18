---
description: Das Error-Objekt gibt die Informationen eines einzelnen Merge-Fehlers zurück.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Error-Objekt (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357607"
---
# <a name="error-object"></a><span data-ttu-id="85285-103">Error-Objekt</span><span class="sxs-lookup"><span data-stu-id="85285-103">Error object</span></span>

<span data-ttu-id="85285-104">Das **Error** -Objekt gibt die Informationen eines einzelnen Merge-Fehlers zurück.</span><span class="sxs-lookup"><span data-stu-id="85285-104">The **Error** object returns the information of a single merge error.</span></span>

## <a name="members"></a><span data-ttu-id="85285-105">Member</span><span class="sxs-lookup"><span data-stu-id="85285-105">Members</span></span>

<span data-ttu-id="85285-106">Das **Error** -Objekt verfügt über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="85285-106">The **Error** object has these types of members:</span></span>

-   [<span data-ttu-id="85285-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85285-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85285-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85285-108">Properties</span></span>

<span data-ttu-id="85285-109">Das **Error** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85285-109">The **Error** object has these properties.</span></span>



| <span data-ttu-id="85285-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="85285-110">Property</span></span>                                                | <span data-ttu-id="85285-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85285-111">Description</span></span>                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85285-112">**Databasekeys**</span><span class="sxs-lookup"><span data-stu-id="85285-112">**DatabaseKeys**</span></span>](error-databasekeys.md)<br/>   | <span data-ttu-id="85285-113">Gibt die Primärschlüssel der Zeile in der Datenbanktabelle zurück, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="85285-113">Returns the primary keys of the row in the database table that caused the error.</span></span><br/> |
| [<span data-ttu-id="85285-114">**Databasetable**</span><span class="sxs-lookup"><span data-stu-id="85285-114">**DatabaseTable**</span></span>](error-databasetable.md)<br/> | <span data-ttu-id="85285-115">Gibt den Tabellennamen der Tabelle in der Datenbank zurück, die den Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="85285-115">Returns the table name of the table in the database causing the error.</span></span><br/>           |
| [<span data-ttu-id="85285-116">**Sprache**</span><span class="sxs-lookup"><span data-stu-id="85285-116">**Language**</span></span>](error-language.md)<br/>           | <span data-ttu-id="85285-117">Gibt die Sprache des Fehlers zurück.</span><span class="sxs-lookup"><span data-stu-id="85285-117">Return the language of the error.</span></span><br/>                                                |
| [<span data-ttu-id="85285-118">**Modulekeys**</span><span class="sxs-lookup"><span data-stu-id="85285-118">**ModuleKeys**</span></span>](error-modulekeys.md)<br/>       | <span data-ttu-id="85285-119">Gibt die Primärschlüssel der Zeile in der Modul Tabelle zurück, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="85285-119">Returns the primary keys of the row in the module table that caused the error.</span></span><br/>   |
| [<span data-ttu-id="85285-120">**Moduletable**</span><span class="sxs-lookup"><span data-stu-id="85285-120">**ModuleTable**</span></span>](error-moduletable.md)<br/>     | <span data-ttu-id="85285-121">Gibt den Tabellennamen der Tabelle im Modul zurück, das den Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="85285-121">Returns the table name of the table in the module causing the error.</span></span><br/>             |
| [<span data-ttu-id="85285-122">**ADS**</span><span class="sxs-lookup"><span data-stu-id="85285-122">**Path**</span></span>](error-path.md)<br/>                   | <span data-ttu-id="85285-123">Gibt den Pfad zur Datei oder zum Verzeichnis zurück, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="85285-123">Return the path to the file or directory causing the error.</span></span> <span data-ttu-id="85285-124">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="85285-124">Currently unused.</span></span><br/>    |
| [<span data-ttu-id="85285-125">**type**</span><span class="sxs-lookup"><span data-stu-id="85285-125">**Type**</span></span>](error-type.md)<br/>                   | <span data-ttu-id="85285-126">Gibt den Typ des Fehlers zurück.</span><span class="sxs-lookup"><span data-stu-id="85285-126">Return the type of error.</span></span><br/>                                                        |



 

## <a name="c"></a><span data-ttu-id="85285-127">C++</span><span class="sxs-lookup"><span data-stu-id="85285-127">C++</span></span>

<span data-ttu-id="85285-128">Schnittstelle **imsmerror: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="85285-128">interface **IMsmError : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="85285-129">Schnittstellen-ID</span><span class="sxs-lookup"><span data-stu-id="85285-129">Interface ID</span></span>



| <span data-ttu-id="85285-130">Konstante</span><span class="sxs-lookup"><span data-stu-id="85285-130">Constant</span></span>           | <span data-ttu-id="85285-131">Wert</span><span class="sxs-lookup"><span data-stu-id="85285-131">Value</span></span>                                  |
|--------------------|----------------------------------------|
| <span data-ttu-id="85285-132">**IID \_ imsmerror**</span><span class="sxs-lookup"><span data-stu-id="85285-132">**IID\_IMsmError**</span></span> | <span data-ttu-id="85285-133">{0adda828-2c26-11d2-Ad65-00a0c9af11a6}</span><span class="sxs-lookup"><span data-stu-id="85285-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="85285-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85285-134">Requirements</span></span>



| <span data-ttu-id="85285-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85285-135">Requirement</span></span> | <span data-ttu-id="85285-136">Wert</span><span class="sxs-lookup"><span data-stu-id="85285-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85285-137">Version</span><span class="sxs-lookup"><span data-stu-id="85285-137">Version</span></span><br/> | <span data-ttu-id="85285-138">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="85285-138">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="85285-139">Header</span><span class="sxs-lookup"><span data-stu-id="85285-139">Header</span></span><br/>  | <dl> <span data-ttu-id="85285-140"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="85285-140"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="85285-141">DLL</span><span class="sxs-lookup"><span data-stu-id="85285-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="85285-142"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85285-142"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




