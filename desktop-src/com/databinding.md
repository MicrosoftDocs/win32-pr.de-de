---
title: Datenbindung
description: Datenbindung
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341965"
---
# <a name="databinding"></a>Datenbindung

Ein neues Datenbindung-Attribut wurde hinzugefügt, um Eigenschaften zu gestatten, unterscheiden zwischen dem Übermitteln von Änderungen nur dann, wenn der Fokus das Steuerelement verlässt oder alle Eigenschaften Änderungs Benachrichtigungen

Das neue-Attribut, das als unmittelatebind bezeichnet wird, ermöglicht es Steuerelementen, zwei verschiedene Typen von bindbaren Eigenschaften zu unterscheiden. Ein Typ der bindbaren Eigenschaft muss jede Änderung an der Datenbank Benachrichtigen, z. b. mit einem Kontrollkästchen-Steuerelement, bei dem jede Änderung an die zugrunde liegende Datenbank gesendet werden muss, auch wenn das Steuerelement den Fokus nicht verliert. Steuerelemente, wie z. b. ein ListBox-Steuerelement, möchten jedoch nur die Änderung einer Eigenschaft an die Datenbank benachrichtigen lassen, wenn das Steuerelement den Fokus verliert, da der Benutzer die markierte Auswahl mit den Pfeiltasten geändert hat, bevor die gewünschte Einstellung gefunden wird, damit die Änderungs Benachrichtigung bei jedem Drücken der Pfeiltaste an die Datenbank gesendet werden kann. Mit der neuen unmittelbaren BIND-Eigenschaft können für einzelne Bindbare Eigenschaften in einem Formular dieses Verhalten angegeben werden. Wenn dieses Bit festgelegt ist, werden alle Änderungen benachrichtigt.

Das neue unmittelatebind-Bit wird durch den neuen varflag-Dateityp " \_ fmmediatebind (0x80)" und das funkflag " \_ dateienbind (0x80)" in den VARFLAGS-und FUNCFLAGS-Enumerationen für die [itypeingefo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) -Schnittstelle zugeordnet, sodass die Properties-Attribute überprüft werden können.

 

 