---
description: Der Zugriffssteuerungs-Editor kann eine Eigenschaftenseite Besitzer enthalten, die es dem Benutzer ermöglicht, einen Objektbesitzer zu ändern. Weitere Informationen zu einem Objektbesitzer finden Sie unter Besitzer eines neuen Objekts und Übernehmen des Objektbesitzes in C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Eigenschaftenseite "Besitzer"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b67b3707017aa8073cfdf4f5ca64340eda74a640bc604a0bd382b7cf2ebe122e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907660"
---
# <a name="owner-property-page"></a>Eigenschaftenseite "Besitzer"

Der Zugriffssteuerungs-Editor kann eine Eigenschaftenseite "Besitzer" enthalten, die es dem Benutzer ermöglicht, den Besitzer eines Objekts zu ändern. Weitere Informationen zum Besitzer eines Objekts finden Sie unter [Besitzer eines neuen Objekts](owner-of-a-new-object.md) und Übernehmen des [Objektbesitzes in C++.](taking-object-ownership-in-c--.md)

Die Eigenschaftenseite **Besitzer** befindet sich auf dem [Eigenschaftenblatt für erweiterte Sicherheit,](advanced-security-property-sheet.md) das angezeigt wird, wenn der Benutzer auf der [Eigenschaftenseite "Grundlegende Sicherheit"](basic-security-property-page.md)auf die Schaltfläche **Erweitert** klickt. Um die **Eigenschaftenseite Besitzer** einzuschließt, legen Sie die \_ SI ADVANCED- und SI EDIT \_ \_ OWNER-Flags in der [**SI OBJECT \_ \_ INFO-Struktur**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) fest, die von Ihrer [**ISecurityInformation::GetObjectInformation-Implementierung**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) zurückgegeben wird.

 

 
