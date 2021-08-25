---
description: Unter 64-Bit-Betriebssystemen kann Windows Installer benutzerdefinierte Aktionen aufrufen, die für 32-Bit- oder 64-Bit-Systeme kompiliert werden.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Verwenden von benutzerdefinierten 64-Bit-Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d94e5d6118c0f2f5dcf5a297718e135cce25a69bea0f48a2d4ea5df4cc0463
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809110"
---
# <a name="using-64-bit-custom-actions"></a>Verwenden von benutzerdefinierten 64-Bit-Aktionen

Unter 64-Bit-Betriebssystemen kann Windows Installer benutzerdefinierte Aktionen aufrufen, die für 32-Bit- oder 64-Bit-Systeme kompiliert werden. Eine benutzerdefinierte 64-Bit-Aktion, die auf [Skripts](scripts.md) basiert, muss explizit als benutzerdefinierte 64-Bit-Aktion markiert werden, indem das **msidbCustomActionType64BitScript-Bit** dem numerischen Aktionstyp in der Spalte Type der [CustomAction-Tabelle](customaction-table.md)hinzugefügt wird. Für benutzerdefinierte [](executable-files.md) Aktionen, die auf ausführbaren Dateien oder [Dynamic Link-Bibliotheken](dynamic-link-libraries.md) basieren, die für 64-Bit-Betriebssysteme unterstützt werden, ist es nicht erforderlich, dieses zusätzliche Bit in die Spalte Typ der CustomAction-Tabelle zu integrieren.

Weitere Informationen finden Sie unter [Benutzerdefinierte 64-Bit-Aktionen.](64-bit-custom-actions.md)

 

 



