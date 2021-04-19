---
description: Der Windows Installer-Dienst verwendet die Sprache des aktuellen Benutzers in allen Dialogfeldern, bis ein Windows Installer Paket geöffnet wird.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Lokalisieren der von Dialogfeldern angezeigten Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353579"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a>Lokalisieren der von Dialogfeldern angezeigten Sprache

Der Windows Installer-Dienst verwendet die Sprache des aktuellen Benutzers in allen Dialogfeldern, bis ein Windows Installer Paket geöffnet wird. Der Windows Installer bestimmt dies mithilfe von **GetUserDefaultUILanguage**. Wenn ein Windows Installer Paket geöffnet wird, zeigt das Installationsprogramm die Dialoge mithilfe der Sprache des Pakets an, wie in der Eigenschaft [**Vorlagen Zusammenfassung**](template-summary.md) angegeben.

Weitere Informationen zum Lokalisieren der Sprache eines Windows Installer Pakets finden Sie unter [ein Beispiel für eine Lokalisierung](a-localization-example.md).

 

 



