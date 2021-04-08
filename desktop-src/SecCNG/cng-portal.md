---
description: CNG ist eine Verschlüsselungs-API, mit der Sie Verschlüsselungs Sicherheitssoftware für die Verschlüsselungsschlüssel Verwaltung, Kryptografie-und Datensicherheit sowie Kryptografie-und Netzwerksicherheit erstellen können.
ms.assetid: eaad88a1-4e1d-4246-9560-8eef60f8b70f
title: 'Kryptografieapi: nächste Generation'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d485f8371905961c63fbab66b29d0db544e3271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861875"
---
# <a name="cryptography-api-next-generation"></a><span data-ttu-id="cdb09-103">Kryptografieapi: nächste Generation</span><span class="sxs-lookup"><span data-stu-id="cdb09-103">Cryptography API: Next Generation</span></span>

## <a name="purpose"></a><span data-ttu-id="cdb09-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="cdb09-104">Purpose</span></span>

<span data-ttu-id="cdb09-105">Cryptography API: Next Generation (CNG) ist die langfristige Ersetzung der [*CryptoAPI*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cdb09-105">Cryptography API: Next Generation (CNG) is the long-term replacement for the [*CryptoAPI*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="cdb09-106">CNG ist so konzipiert, dass es auf vielen Ebenen erweiterbar und im Verhalten kryptografieagnostisch ist.</span><span class="sxs-lookup"><span data-stu-id="cdb09-106">CNG is designed to be extensible at many levels and cryptography agnostic in behavior.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="cdb09-107">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="cdb09-107">Developer audience</span></span>

<span data-ttu-id="cdb09-108">CNG ist für die Verwendung durch Entwickler von Anwendungen gedacht, die es Benutzern ermöglichen, Dokumente und andere Daten in einer sicheren Umgebung zu erstellen und auszutauschen, insbesondere über nicht sichere Medien wie das Internet.</span><span class="sxs-lookup"><span data-stu-id="cdb09-108">CNG is intended for use by developers of applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="cdb09-109">Entwickler sollten mit den Programmiersprachen C und C++ und der Windows-basierten Programmierumgebung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="cdb09-109">Developers should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="cdb09-110">Es ist zwar nicht erforderlich, aber es wird empfohlen, Kryptografie-oder sicherheitsrelevante Themen zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="cdb09-110">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="cdb09-111">Wenn Sie einen CNG-kryptografiealgorithmusanbieter oder einen Schlüsselspeicher Anbieter entwickeln, müssen Sie das [kryptografieanbieterentwicklungskit](https://www.microsoft.com/download/details.aspx?id=30688) von Microsoft herunterladen.</span><span class="sxs-lookup"><span data-stu-id="cdb09-111">If you are developing a CNG cryptographic algorithm provider or key storage provider, you must download the [Cryptographic Provider Development Kit](https://www.microsoft.com/download/details.aspx?id=30688) from Microsoft.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="cdb09-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="cdb09-112">Run-time requirements</span></span>

<span data-ttu-id="cdb09-113">CNG wird ab Windows Server 2008 und Windows Vista unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cdb09-113">CNG is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="cdb09-114">Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="cdb09-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cdb09-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cdb09-115">In this section</span></span>



| <span data-ttu-id="cdb09-116">Thema</span><span class="sxs-lookup"><span data-stu-id="cdb09-116">Topic</span></span>                                         | <span data-ttu-id="cdb09-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cdb09-117">Description</span></span>                                                                                                                                    |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdb09-118">Informationen über CNG</span><span class="sxs-lookup"><span data-stu-id="cdb09-118">About CNG</span></span>](about-cng.md)<br/>         | <span data-ttu-id="cdb09-119">Beschreibt CNG-Funktionen, kryptografieprimitive und Schlüssel Speicherung, Abruf, Import und Export.</span><span class="sxs-lookup"><span data-stu-id="cdb09-119">Describes CNG features, cryptographic primitives, and key storage, retrieval, import, and export.</span></span><br/>                                   |
| [<span data-ttu-id="cdb09-120">Verwenden von CNG</span><span class="sxs-lookup"><span data-stu-id="cdb09-120">Using CNG</span></span>](using-cng.md)<br/>         | <span data-ttu-id="cdb09-121">Erläutert die Verwendung der kryptografiekonfigurationsfeatures von CNG und typischer CNG-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="cdb09-121">Explains how to use the cryptography configuration features of CNG and typical CNG programming.</span></span><br/>                                     |
| [<span data-ttu-id="cdb09-122">CNG-Verweis</span><span class="sxs-lookup"><span data-stu-id="cdb09-122">CNG Reference</span></span>](cng-reference.md)<br/> | <span data-ttu-id="cdb09-123">Ausführliche Beschreibungen der CNG-Programmier Elemente.</span><span class="sxs-lookup"><span data-stu-id="cdb09-123">Detailed descriptions of the CNG programming elements.</span></span> <span data-ttu-id="cdb09-124">Diese Seiten enthalten Referenz Beschreibungen der API für die Arbeit mit CNG.</span><span class="sxs-lookup"><span data-stu-id="cdb09-124">These pages include reference descriptions of the API for working with CNG.</span></span> <br/> |



 

 

