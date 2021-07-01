---
description: Beschreibt die Neuerungen für Dokumente und das Drucken in Windows 7.
ms.assetid: 3338df74-f895-4389-875c-5a61f18fc690
title: Neuerungen beim Drucken in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cdae3196aa47ed0685fccf97a12b61d5839d61
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119385"
---
# <a name="whats-new-for-printing-in-windows-7"></a><span data-ttu-id="5ed3f-103">Neuerungen beim Drucken in Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ed3f-103">What's New for Printing in Windows 7</span></span>

<span data-ttu-id="5ed3f-104">Beschreibt die Neuerungen für Dokumente und das Drucken in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5ed3f-104">Describes what is new for documents and printing in Windows 7.</span></span>

## <a name="documents-and-printing"></a><span data-ttu-id="5ed3f-105">Dokumente und Drucken </span><span class="sxs-lookup"><span data-stu-id="5ed3f-105">Documents and Printing</span></span>

<span data-ttu-id="5ed3f-106">Dokumente und Das Drucken wurde für Windows 7 verbessert, um die folgenden neuen Features und Verbesserungen zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="5ed3f-106">Documents and printing has been improved for Windows 7 to include the following new features and enhancements.</span></span>



| <span data-ttu-id="5ed3f-107">Dokumenttechnologie</span><span class="sxs-lookup"><span data-stu-id="5ed3f-107">Document technology</span></span>                                                                                                                | <span data-ttu-id="5ed3f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ed3f-108">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed3f-109">[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ed3f-109">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span><br/>                                                        | <span data-ttu-id="5ed3f-110">Mit der [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) können Sie XPS-Dokumente aus Ihrem Win32-Programm erstellen und als Dokumentdatei speichern oder direkt an einen Drucker senden.</span><span class="sxs-lookup"><span data-stu-id="5ed3f-110">The [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) lets you create XPS documents from your Win32 program and save them as a document file or send them directly to a printer.</span></span><br/> <span data-ttu-id="5ed3f-111">Sie können auch die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) verwenden, um vorhandene XPS-Dokumente in einem Win32-Programm zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5ed3f-111">You can also use the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to modify existing XPS documents in a Win32 program.</span></span><br/> |
| <span data-ttu-id="5ed3f-112">[API für digitale XPS-Signaturen](/previous-versions/windows/desktop/ff819108(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ed3f-112">[XPS Digital Signature API](/previous-versions/windows/desktop/ff819108(v=vs.85))</span></span><br/>                                      | <span data-ttu-id="5ed3f-113">Mit der [XPS Digital Signature-API](/previous-versions/windows/desktop/ff819108(v=vs.85)) können Sie XPS-Dokumenten aus Ihrem Win32-Programm digitale Signaturen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5ed3f-113">The [XPS Digital Signature API](/previous-versions/windows/desktop/ff819108(v=vs.85)) lets you add digital signatures to XPS documents from your Win32 program.</span></span><br/> <span data-ttu-id="5ed3f-114">Sie können auch die DIGITALE XPS-Signatur-API verwenden, um zu überprüfen, ob ein XPS-Dokument authentifiziert und unverändert ist.</span><span class="sxs-lookup"><span data-stu-id="5ed3f-114">You can also use the XPS Digital Signature API to verify whether an XPS document is authentic and unaltered.</span></span><br/>                                          |
| [<span data-ttu-id="5ed3f-115">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="5ed3f-115">XPS Print API</span></span>](xps-printing.md)<br/>                                                                   | <span data-ttu-id="5ed3f-116">Mit der [XPS-Druck-API](xpsprint-api.md) können Sie XPS-Dokumente aus Ihrem Win32-Programm drucken.</span><span class="sxs-lookup"><span data-stu-id="5ed3f-116">The [XPS Print API](xpsprint-api.md) lets you print XPS documents from your Win32 program.</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="5ed3f-117">Verbesserungen am [Microsoft XPS-Dokumentkonverter (MXDC)](microsoft-xps-document-converter--mxdc-.md)</span><span class="sxs-lookup"><span data-stu-id="5ed3f-117">[Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) improvements</span></span><br/> | <span data-ttu-id="5ed3f-118">Das [MXDC](microsoft-xps-document-converter--mxdc-.md) wurde verbessert, sodass Sie vorhandene GDI-Funktionen verwenden können, um XPS-Inhalte zu erstellen und in den XPS-Druckpfad aus Ihren Win32-Programmen zu drucken, und zwar mit einer höheren grafischen Genauigkeit als in Windows Vista möglich.</span><span class="sxs-lookup"><span data-stu-id="5ed3f-118">The [MXDC](microsoft-xps-document-converter--mxdc-.md) has been improved so that you can use existing GDI functionality to create XPS content and print to the XPS print path from your Win32 programs with greater graphical fidelity than was possible in Windows Vista.</span></span><br/>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="5ed3f-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ed3f-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5ed3f-120">[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ed3f-120">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5ed3f-121">[API für digitale XPS-Signaturen](/previous-versions/windows/desktop/ff819108(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ed3f-121">[XPS Digital Signature API](/previous-versions/windows/desktop/ff819108(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5ed3f-122">XPS-Druck-API</span><span class="sxs-lookup"><span data-stu-id="5ed3f-122">XPS Print API</span></span>](xpsprint-api.md)
</dt> </dl>

 

