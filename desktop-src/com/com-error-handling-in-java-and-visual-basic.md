---
title: COM-Fehlerbehandlung in Java und Visual Basic
description: COM-Fehlerbehandlung in Java und Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424010"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="c8644-103">COM-Fehlerbehandlung in Java und Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c8644-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="c8644-104">Es gibt drei Schnittstellen und drei Funktionen, die in COM verwendet werden können, um fehlerbehandlung bei der Programmierung in Java oder Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c8644-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="c8644-105">In Java und Visual Basic gibt der Methodenaufruf kein **HRESULT** als Rückgabewert zurück.</span><span class="sxs-lookup"><span data-stu-id="c8644-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="c8644-106">Stattdessen verwenden diese Sprachen die COM-Schnittstellen und -Funktionen, um **HRESULT-Werte** zu erhalten und Fehler oder Ausnahmen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="c8644-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="c8644-107">(Ausnahmen sind Ereignisse, die außerhalb der Kontrolle des Programms liegen, z. B. Dateiprobleme oder ungültige Parameter.)</span><span class="sxs-lookup"><span data-stu-id="c8644-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="c8644-108">Die drei Schnittstellen, die **HRESULT-Unterstützung** bieten, sind in der folgenden Tabelle kurz aufgeführt und beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c8644-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|  <span data-ttu-id="c8644-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c8644-109">Interface</span></span>                                                                        |  <span data-ttu-id="c8644-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8644-110">Description</span></span>                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8644-111">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c8644-111">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="c8644-112">Legt Fehlerinformationen fest.</span><span class="sxs-lookup"><span data-stu-id="c8644-112">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="c8644-113">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c8644-113">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="c8644-114">Gibt Informationen aus einem Fehlerobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c8644-114">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="c8644-115">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c8644-115">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="c8644-116">Identifiziert das -Objekt als unterstützung für die [**IErrorInfo-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)</span><span class="sxs-lookup"><span data-stu-id="c8644-116">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="c8644-117">Die drei Funktionen, die **HRESULT-Unterstützung** bieten, sind in der folgenden Tabelle kurz aufgeführt und beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c8644-117">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|    <span data-ttu-id="c8644-118">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c8644-118">Interface</span></span>       |       <span data-ttu-id="c8644-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8644-119">Description</span></span>       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8644-120">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c8644-120">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="c8644-121">Erstellt eine Instanz eines generischen Fehlerobjekts.</span><span class="sxs-lookup"><span data-stu-id="c8644-121">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="c8644-122">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c8644-122">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="c8644-123">Erhält den Fehlerinformationszeiger, der durch den vorherigen Aufruf von [**SetErrorInfo im**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) aktuellen logischen Thread festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="c8644-123">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="c8644-124">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c8644-124">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="c8644-125">Legt das Fehlerinformationsobjekt für den aktuellen Ausführungsthread fest.</span><span class="sxs-lookup"><span data-stu-id="c8644-125">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="c8644-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8644-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8644-127">Fehlerbehandlung in COM</span><span class="sxs-lookup"><span data-stu-id="c8644-127">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

