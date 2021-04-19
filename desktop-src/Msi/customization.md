---
description: Da der Windows Installer alle Informationen zur Installation in einer relationalen Datenbank beibehält, kann die Installation einer Anwendung oder eines Produkts für bestimmte Benutzergruppen angepasst werden, indem Transformations Vorgänge auf das Paket angewendet werden.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Anpassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346976"
---
# <a name="customization"></a>Anpassung

Da der Windows Installer alle Informationen zur Installation in einer relationalen Datenbank beibehält, kann die Installation einer Anwendung oder eines Produkts für bestimmte Benutzergruppen angepasst werden, indem Transformations Vorgänge auf das Paket angewendet werden. Transformationen können verwendet werden, um die verschiedenen Anpassungen eines Basispakets zu kapseln, das von unterschiedlichen Arbeitsgruppen benötigt wird. Weitere Informationen finden Sie unter Zusammenführungen [und Transformationen](merges-and-transforms.md).

Mehrere Transformationen eines Basispakets können während der Installation dynamisch angewendet werden. Dies bietet einen Mechanismus, mit dem benutzerdefinierte Installationen unterschiedlichen Benutzergruppen effizient zugewiesen werden können. Dies wäre z. b. in Organisationen hilfreich, in denen die Support Abteilungen für Finanzabteilung und Personal verschiedene Installationen eines bestimmten Produkts benötigen. Das Produkt kann allen Benutzern in der Organisation durch eine [Administrative Installation](administrative-installation.md) des Basispakets an einen einzelnen administrativen Installations Punkt zur Verfügung gestellt werden. Jede Arbeitsgruppe kann dann automatisch Ihre geeignete Anpassung über eine dynamische Transformation erhalten, wenn Sie das Produkt installieren.

 

 



