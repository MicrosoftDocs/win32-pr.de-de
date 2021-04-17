---
title: COM-Fehlerbehandlung in Java und Visual Basic
description: COM-Fehlerbehandlung in Java und Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea12dc040218e14098ce2394fbb5cd2ebeff1704
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391066"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="864d6-103">COM-Fehlerbehandlung in Java und Visual Basic</span><span class="sxs-lookup"><span data-stu-id="864d6-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="864d6-104">Es gibt drei Schnittstellen und drei Funktionen, die in com verwendet werden können, um Fehlerbehandlung bei der Programmierung in Java oder Microsoft Visual Basic bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="864d6-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="864d6-105">In Java und Visual Basic gibt der Methoden Aufrufwert kein **HRESULT** als Rückgabewert zurück.</span><span class="sxs-lookup"><span data-stu-id="864d6-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="864d6-106">Stattdessen verwenden diese Sprachen die COM-Schnittstellen und-Funktionen zum Abrufen von **HRESULT** -Werten und zum Behandeln von Fehlern oder Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="864d6-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="864d6-107">(Ausnahmen sind Ereignisse, die über das Programm gesteuert werden, wie z. b. Datei Probleme oder ungültige Parameter.)</span><span class="sxs-lookup"><span data-stu-id="864d6-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="864d6-108">Die drei Schnittstellen, die **HRESULT** s unterstützen, werden in der folgenden Tabelle aufgeführt und kurz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="864d6-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                          |                                                                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="864d6-109">**Ikreateerrorinfo**</span><span class="sxs-lookup"><span data-stu-id="864d6-109">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="864d6-110">Legt Fehlerinformationen fest.</span><span class="sxs-lookup"><span data-stu-id="864d6-110">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="864d6-111">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="864d6-111">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="864d6-112">Gibt Informationen von einem Fehler Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="864d6-112">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="864d6-113">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="864d6-113">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="864d6-114">Identifiziert das-Objekt als Unterstützung der [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="864d6-114">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="864d6-115">Die drei Funktionen, die **HRESULT** s unterstützen, werden in der folgenden Tabelle aufgeführt und kurz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="864d6-115">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                        |                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="864d6-116">**"Kreateerrorinfo"**</span><span class="sxs-lookup"><span data-stu-id="864d6-116">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="864d6-117">Erstellt eine Instanz eines generischen Fehler Objekts.</span><span class="sxs-lookup"><span data-stu-id="864d6-117">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="864d6-118">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="864d6-118">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="864d6-119">Ruft den Fehler Informations Zeiger ab, der durch den vorherigen Aufrufs von [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) im aktuellen logischen Thread festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="864d6-119">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="864d6-120">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="864d6-120">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="864d6-121">Legt das Fehler Informationsobjekt für den aktuellen Ausführungs Thread fest.</span><span class="sxs-lookup"><span data-stu-id="864d6-121">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="864d6-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="864d6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="864d6-123">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="864d6-123">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

