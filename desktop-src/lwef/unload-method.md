---
title: Unload-Methode
description: Unload-Methode
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74f274f758e34416cc73d82963fa21fbd93b14e7b6492c693f24b763081b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474498"
---
# <a name="unload-method"></a>Unload-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Entlädt die Zeichendaten für das angegebene Zeichen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Characters.Unload "**_CharacterID_*_"_*

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, wenn Sie kein Zeichen mehr benötigen, um Arbeitsspeicher freizugeben, der zum Speichern von Informationen über das Zeichen verwendet wird. Wenn Sie erneut auf das Zeichen zugreifen, verwenden Sie die [**Load-Methode.**](load-method.md)

Diese Methode gibt kein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurück.

 

 