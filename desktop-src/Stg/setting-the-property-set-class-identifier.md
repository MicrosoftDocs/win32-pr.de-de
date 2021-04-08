---
title: Festlegen des Eigenschafts Satz-Klassen Bezeichners
description: Die IPropertyStorage-setClass-Methode legt sowohl die CLSID des Speicher Objekts als auch den Wert des Klassentags fest, der im com-Eigenschaften Satz gespeichert ist. Dies tritt auf, wenn für einen nicht einfachen Eigenschafts Speicher aufgerufen wird, der in einem strukturierten Speicher Objekt gespeichert ist.
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- Festlegen des Eigenschafts Satz-Klassen Bezeichners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037403"
---
# <a name="setting-the-property-set-class-identifier"></a>Festlegen des Eigenschafts Satz-Klassen Bezeichners

Die [**IPropertyStorage:: setClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) -Methode legt sowohl die CLSID des Speicher Objekts als auch den Wert des Klassentags fest, der im com-Eigenschaften Satz gespeichert ist. Dies tritt auf, wenn für einen nicht einfachen Eigenschafts Speicher aufgerufen wird, der in einem strukturierten Speicher Objekt gespeichert ist.

Dies bietet Konsistenz und Einheitlichkeit, wodurch eine bessere Interaktion mit einigen Tools erzielt wird. Ein Eigenschaften Speicher Objekt ist nicht einfach, wenn es durch Aufrufen von [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) mit dem **\_ nicht einfachen Flag propsetflag** erstellt wird.

Die CLSID des Speicher Objekts wird mit einem Aufrufen von [**IStorage:: setClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)festgelegt.

 

 




