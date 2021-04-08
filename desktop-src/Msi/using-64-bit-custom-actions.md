---
description: Auf 64-Bit-Betriebssystemen können Windows Installer benutzerdefinierte Aktionen aufzurufen, die für 32-Bit-oder 64-Bit-Systeme kompiliert werden.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Verwenden von benutzerdefinierten 64-Bit-Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960147"
---
# <a name="using-64-bit-custom-actions"></a>Verwenden von benutzerdefinierten 64-Bit-Aktionen

Auf 64-Bit-Betriebssystemen können Windows Installer benutzerdefinierte Aktionen aufzurufen, die für 32-Bit-oder 64-Bit-Systeme kompiliert werden. Eine benutzerdefinierte 64-Bit-Aktion, die auf [Skripts](scripts.md) basiert, muss explizit als 64 eine benutzerdefinierte 32-Bit-Aktion gekennzeichnet werden, indem das **msidbCustomActionType64BitScript** -Bit dem numerischen Typ benutzerdefinierte Aktion in der Type-Spalte der [CustomAction-Tabelle](customaction-table.md)hinzugefügt wird. Benutzerdefinierte Aktionen, die auf [ausführbaren Dateien](executable-files.md) oder [Dynamic Link-Bibliotheken](dynamic-link-libraries.md) basieren, die für 64-Bit-Betriebssysteme erfüllt werden, müssen dieses zusätzliche Bit nicht in die Spalte Type der Tabelle CustomAction einschließen.

Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).

 

 



