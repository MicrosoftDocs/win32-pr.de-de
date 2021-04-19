---
description: '\_Benutzerdefinierte Gebiets Schema \* Konstanten'
ms.assetid: a41a7f55-8905-47a1-86c3-74ed40b3834c
title: LOCALE_CUSTOM *-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4e02cc672241fd609a5eda975c0e9e13d29908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346892"
---
# <a name="locale_custom-constants"></a>\_Benutzerdefinierte Gebiets Schema \* Konstanten

In diesem Thema werden die \_ benutzerdefinierten benutzerdefinierten \* Konstanten von NLS zum Darstellen von [benutzerdefinierten](custom-locales.md)Gebiets Schemas definiert.



| Wert                       | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_benutzerdefinierter locale- \_ Standard     | **Windows Vista und höher:** Das standardmäßige benutzerdefinierte Gebiets Schema. Wenn eine NLS-Funktion einen Gebiets Schema Bezeichner für ein [zusätzliches](custom-locales.md) Gebiets Schema für den aktuellen Benutzer zurückgeben muss, gibt die Funktion diesen Wert anstelle von [locale \_ User \_ default](locale-user-default.md)zurück. Der \_ benutzerdefinierte locale- \_ Standardwert ist 0x0c00.                                                                                                                                                                  |
| benutzerdefinierte Benutzeroberflächen- \_ \_ \_ Standardeinstellung | **Windows Vista und höher:** Das standardmäßige benutzerdefinierte Gebiets Schema für MUI. Die bevorzugten Benutzeroberflächen Sprachen und die bevorzugten Benutzeroberflächen Sprachen des Benutzers können höchstens eine Sprache enthalten, die von einem Language Interface Pack (LIP) implementiert wird und für die der sprach Bezeichner einem ergänzenden Gebiets Schema entspricht. Wenn eine solche Sprache in einer Liste vorhanden ist, wird die Konstante verwendet, um in bestimmten Kontexten auf diese Sprache zu verweisen. Der Standardwert des benutzerdefinierten Gebiets Schemas der \_ Benutzer \_ Oberfläche \_ ist 0x1400.                    |
| Gebiets Schema \_ Benutzer \_ definiert nicht angegeben | **Windows Vista und höher:** Ein nicht angegebenes benutzerdefiniertes Gebiets Schema, mit dem alle ergänzenden Gebiets Schemata außer dem Gebiets Schema des aktuellen Benutzers identifiziert werden. Ergänzende Gebiets Schemata können nicht durch ihre Gebiets Schema Bezeichner voneinander unterschieden werden, Sie können jedoch anhand ihrer Gebiets Schema [Namen](locale-names.md)unterschieden werden. Bestimmte nls-Funktionen können diese Konstante zurückgeben, um anzugeben, dass Sie keinen nützlichen Bezeichner für ein bestimmtes Gebiets Schema bereitstellen können. Der Wert des benutzerdefinierten Gebiets Schemas \_ \_ nicht angegeben ist 0x1000. |



 

 

 



