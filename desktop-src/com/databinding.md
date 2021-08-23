---
title: Datenbindung
description: Datenbindung
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c2040aa29c83615f42c321483c87be378737dcdef47e43873fbe3b8c0902dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048368"
---
# <a name="databinding"></a>Datenbindung

Es wurde ein neues Datenbindungsattribut hinzugefügt, mit dem Eigenschaften zwischen der Kommunikation von Änderungen nur dann unterschieden werden können, wenn der Fokus das Steuerelement verlässt, oder bei allen Benachrichtigungen zu Eigenschaftenänderungen.

Das neue Attribut, bekannt als ImmediateBind, ermöglicht es Steuerelementen, zwei verschiedene Typen von bindbaren Eigenschaften zu unterscheiden. Ein Typ einer bindbaren Eigenschaft muss jede Änderung an der Datenbank benachrichtigen, z. B. mit einem Kontrollkästchen-Steuerelement, bei dem jede Änderung an die zugrunde liegende Datenbank gesendet werden muss, obwohl das Steuerelement nicht den Fokus verloren hat. Steuerelemente wie z. B. ein Listenfeld möchten jedoch nur die Änderung einer Eigenschaft an die Datenbank senden lassen, wenn das Steuerelement den Fokus verliert, da der Benutzer die hervorgehobene Auswahl möglicherweise mit den Pfeiltasten geändert hat, bevor er die gewünschte Einstellung findet, damit die Änderungsbenachrichtigung jedes Mal an die Datenbank gesendet wird, wenn der Benutzer auf die Pfeiltaste trifft, eine inakzeptable Leistung erzielen würde. Die neue Eigenschaft für die sofortige Bindung ermöglicht es einzelnen bindbaren Eigenschaften in einem Formular, dieses Verhalten anzugeben, wenn dieses Bit festgelegt ist, werden alle Änderungen benachrichtigt.

Das neue ImmediateBind-Bit wird den neuen VARFLAG \_ FIMMEDIATEBIND (0x80) und den FUNCFLAG \_ FIMMEDIATEBIND (0x80)-Bits in den VARFLAGS- und FUNCFLAGS-Enumerationen für die [ITypeInfo-Schnittstelle](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) durchgepasst, sodass die Eigenschaftenattribute überprüft werden können.

 

 