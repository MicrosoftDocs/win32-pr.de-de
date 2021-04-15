---
title: LST-Tag
description: LST-Tag
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515747"
---
# <a name="lst-tag"></a><span data-ttu-id="527da-103">LST-Tag</span><span class="sxs-lookup"><span data-stu-id="527da-103">Lst Tag</span></span>

<span data-ttu-id="527da-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="527da-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="527da-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="527da-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="527da-106">Wiederholt die letzte gesprochene Anweisung für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="527da-106">Repeats last spoken statement for the character.</span></span>

</dd> <dt>

<span data-ttu-id="527da-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="527da-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="527da-108">\\**LST**</span><span class="sxs-lookup"><span data-stu-id="527da-108">\\**Lst**</span></span>\\

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="527da-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="527da-109">Remarks</span></span>

<span data-ttu-id="527da-110">Mit diesem Tag kann ein Zeichen seine letzte gesprochene Anweisung wiederholen.</span><span class="sxs-lookup"><span data-stu-id="527da-110">This tag enables a character to repeat its last spoken statement.</span></span> <span data-ttu-id="527da-111">Dieses Tag muss in der [**Sprech**](speak-method.md) Methode eigenständig angezeigt werden. Es können keine anderen Text oder Parameter eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="527da-111">This tag must appear by itself in the [**Speak**](speak-method.md) method; no other text or parameters can be included.</span></span> <span data-ttu-id="527da-112">Wenn der gesprochene Text wiederholt wird, werden alle anderen im ursprünglichen Text enthaltenen Tags wiederholt, mit Ausnahme von Lesezeichen.</span><span class="sxs-lookup"><span data-stu-id="527da-112">When the spoken text is repeated, any other tags included in the original text are repeated, except for bookmarks.</span></span> <span data-ttu-id="527da-113">Irgendeiner. WAV und. Lwv-Dateien, die im Text enthalten sind, werden ebenfalls wiederholt.</span><span class="sxs-lookup"><span data-stu-id="527da-113">Any .WAV and .LWV files included in the text are also repeated.</span></span>

 

 




