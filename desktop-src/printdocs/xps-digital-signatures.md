---
description: Mit der XPS Digital Signature-API kann ein Benutzer ein Dokument signieren, die Identität des Signatur Gebers überprüfen und angeben, ob ein XPS-Dokument seit der Signierung geändert wurde.
ms.assetid: 8a23617e-92fe-4662-b602-47add5716358
title: XPS-API für digitale Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c56485a532afbb148e62901c38db49ab81963c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350877"
---
# <a name="xps-digital-signature-api"></a><span data-ttu-id="69b8b-103">XPS-API für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="69b8b-103">XPS Digital Signature API</span></span>

<span data-ttu-id="69b8b-104">Mit der XPS Digital Signature-API kann ein Benutzer ein Dokument signieren, die Identität des Signatur Gebers überprüfen und angeben, ob ein XPS-Dokument seit der Signierung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="69b8b-104">The XPS Digital Signature API enables a user to sign a document, verify the identity of the signer, and indicate whether an XPS document has changed since it was signed.</span></span> <span data-ttu-id="69b8b-105">Die API für die digitale Signatur von XPS basiert auf der digitalen Signatur Technologie, die in den Open Packaging-Konventionen verwendet wird, die in der ersten Edition, Teil 2, "Open Packaging Conventions", in den [Standard mäßigen ECMA-376-und Office Open XML-Dateiformaten](https://www.ecma-international.org/publications/standards/Ecma-376.htm)festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="69b8b-105">The XPS Digital Signature API is built on the digital signature technology that is used in the Open Packaging Conventions, which are specified in the 1st edition, Part 2, "Open Packaging Conventions," of [Standard ECMA-376, Office Open XML File Formats](https://www.ecma-international.org/publications/standards/Ecma-376.htm).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69b8b-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="69b8b-106">In This Section</span></span>

<span data-ttu-id="69b8b-107">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="69b8b-107">This section contains the following topics.</span></span>

### <a name="about-xps-digital-signature-api"></a><span data-ttu-id="69b8b-108">Informationen über die XPS Digital Signature-API</span><span class="sxs-lookup"><span data-stu-id="69b8b-108">About XPS Digital Signature API</span></span>

<span data-ttu-id="69b8b-109">[Informationen zur digitalen Signatur-API von XPS](about-xps-digital-signatures.md) beschreiben die API für die digitale Signatur von XPS auf hoher Ebene.</span><span class="sxs-lookup"><span data-stu-id="69b8b-109">[About XPS Digital Signature API](about-xps-digital-signatures.md) describes the XPS Digital Signature API at a high level.</span></span>

### <a name="using-xps-digital-signature-api"></a><span data-ttu-id="69b8b-110">Verwenden der XPS Digital-Signatur-API</span><span class="sxs-lookup"><span data-stu-id="69b8b-110">Using XPS Digital Signature API</span></span>

<span data-ttu-id="69b8b-111">[Mithilfe der XPS Digital Signature-API](using-digital-signatures-in-xps-documents.md) wird beschrieben, wie Sie die XPS Digital Signature-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="69b8b-111">[Using XPS Digital Signature API](using-digital-signatures-in-xps-documents.md) describes how to use the XPS Digital Signature API.</span></span>

### <a name="xps-digital-signatures-reference"></a><span data-ttu-id="69b8b-112">XPS-Referenz für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="69b8b-112">XPS Digital Signatures Reference</span></span>

<span data-ttu-id="69b8b-113">Die [XPS Digital Signature-API-Referenz](xps-digital-signatures-programming-reference.md) enthält eine komplette Liste der Schnittstellen, Methoden und Enumeratoren, die von der XPS Digital Signature-API implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="69b8b-113">The [XPS Digital Signature API Reference](xps-digital-signatures-programming-reference.md) contains a complete listing of the interfaces, methods, and enumerators that are implemented by the XPS Digital Signatures API.</span></span>

## <a name="platform-update-for-windows-vista"></a><span data-ttu-id="69b8b-114">Platt Form Update für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69b8b-114">Platform Update for Windows Vista</span></span>

<span data-ttu-id="69b8b-115">Die in diesem Abschnitt beschriebenen XPS-Schnittstellen für digitale Signaturen werden vom Platt Form Update für Windows Vista oder dem Platt Form Update für Windows Server 2008 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="69b8b-115">The XPS Digital Signature interfaces that are described in this section are not supported by the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="69b8b-116">Eine Anwendung, die diese Schnittstellen erfordert, sollte unter Windows 7 oder höher oder Windows Server 2008 R2 oder höher ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="69b8b-116">An application that requires these interfaces should run on Windows 7 or later, or on Windows Server 2008 R2 or later.</span></span> <span data-ttu-id="69b8b-117">Andernfalls stellt die Anwendung dem Benutzer möglicherweise nicht die gesamte Funktionalität der Anwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="69b8b-117">Otherwise, the application may not provide the user with the application's complete functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69b8b-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69b8b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69b8b-119">Verpackung</span><span class="sxs-lookup"><span data-stu-id="69b8b-119">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="69b8b-120">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="69b8b-120">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="69b8b-121">Standard-ECMA-376, Office Open XML-Dateiformate</span><span class="sxs-lookup"><span data-stu-id="69b8b-121">Standard ECMA-376, Office Open XML File Formats</span></span>](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
