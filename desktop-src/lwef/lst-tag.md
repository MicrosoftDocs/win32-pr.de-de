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
# <a name="lst-tag"></a>LST-Tag

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Wiederholt die letzte gesprochene Anweisung für das Zeichen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

\\**LST**\\

</dd> </dl>

### <a name="remarks"></a>Bemerkungen

Mit diesem Tag kann ein Zeichen seine letzte gesprochene Anweisung wiederholen. Dieses Tag muss in der [**Sprech**](speak-method.md) Methode eigenständig angezeigt werden. Es können keine anderen Text oder Parameter eingeschlossen werden. Wenn der gesprochene Text wiederholt wird, werden alle anderen im ursprünglichen Text enthaltenen Tags wiederholt, mit Ausnahme von Lesezeichen. Irgendeiner. WAV und. Lwv-Dateien, die im Text enthalten sind, werden ebenfalls wiederholt.

 

 




