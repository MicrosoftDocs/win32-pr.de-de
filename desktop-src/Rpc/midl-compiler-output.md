---
title: Mittel l-Compilerausgabe
description: Wenn die IDL-und ACF-Dateien als Eingabe erstellt werden, generiert der-compilercompiler bis zu fünf Quelldateien der C-Sprache.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036596"
---
# <a name="midl-compiler-output"></a><span data-ttu-id="78d80-103">Mittel l-Compilerausgabe</span><span class="sxs-lookup"><span data-stu-id="78d80-103">MIDL Compiler Output</span></span>

<span data-ttu-id="78d80-104">Wenn die IDL-und ACF-Dateien als Eingabe erstellt werden, generiert der-compilercompiler bis zu fünf Quelldateien der C-Sprache.</span><span class="sxs-lookup"><span data-stu-id="78d80-104">With the IDL and ACF files as input, the MIDL compiler generates up to five C-language source files.</span></span> <span data-ttu-id="78d80-105">Standardmäßig verwendet der mittlerer l-Compiler den Basis Dateinamen der IDL-Datei als Teil der generierten Stubdateien.</span><span class="sxs-lookup"><span data-stu-id="78d80-105">By default, the MIDL compiler uses the base file name of the IDL file as part of the generated stub files.</span></span> <span data-ttu-id="78d80-106">Wenn im Basis Dateinamen mehr als sechs Zeichen vorhanden sind, akzeptieren einige Dateisysteme möglicherweise nicht den vollständigen Stub-Namen.</span><span class="sxs-lookup"><span data-stu-id="78d80-106">When more than six characters are present in the base file name, some file systems may not accept the full stub name.</span></span> <span data-ttu-id="78d80-107">In der folgenden Tabelle sind die für Dateinamen verwendeten Konventionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="78d80-107">The following table shows conventions used for file names.</span></span>



| <span data-ttu-id="78d80-108">File</span><span class="sxs-lookup"><span data-stu-id="78d80-108">File</span></span>        | <span data-ttu-id="78d80-109">Standardabschnitt des Basis Dateinamens</span><span class="sxs-lookup"><span data-stu-id="78d80-109">Default portion of base file name</span></span> | <span data-ttu-id="78d80-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="78d80-110">Example</span></span>      |
|-------------|-----------------------------------|--------------|
| <span data-ttu-id="78d80-111">IDL-Datei</span><span class="sxs-lookup"><span data-stu-id="78d80-111">IDL file</span></span>    | ---                               | <span data-ttu-id="78d80-112">ABCDEFGH. idl</span><span class="sxs-lookup"><span data-stu-id="78d80-112">Abcdefgh.idl</span></span> |
| <span data-ttu-id="78d80-113">Header</span><span class="sxs-lookup"><span data-stu-id="78d80-113">Header</span></span>      | <span data-ttu-id="78d80-114">.h</span><span class="sxs-lookup"><span data-stu-id="78d80-114">.h</span></span>                                | <span data-ttu-id="78d80-115">Abcdef. h</span><span class="sxs-lookup"><span data-stu-id="78d80-115">Abcdef.h</span></span>     |
| <span data-ttu-id="78d80-116">Clientstub</span><span class="sxs-lookup"><span data-stu-id="78d80-116">Client stub</span></span> | <span data-ttu-id="78d80-117">\_c. c</span><span class="sxs-lookup"><span data-stu-id="78d80-117">\_c.c</span></span>                             | <span data-ttu-id="78d80-118">Abcdef \_ c. c</span><span class="sxs-lookup"><span data-stu-id="78d80-118">Abcdef\_c.c</span></span>  |
| <span data-ttu-id="78d80-119">Server-Stub</span><span class="sxs-lookup"><span data-stu-id="78d80-119">Server stub</span></span> | <span data-ttu-id="78d80-120">\_s. c</span><span class="sxs-lookup"><span data-stu-id="78d80-120">\_s.c</span></span>                             | <span data-ttu-id="78d80-121">Abcdef \_ s. c</span><span class="sxs-lookup"><span data-stu-id="78d80-121">Abcdef\_s.c</span></span>  |



 

 

 




