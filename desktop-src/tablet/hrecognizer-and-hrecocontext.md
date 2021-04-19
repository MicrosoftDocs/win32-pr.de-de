---
description: Sie verweisen auf eine Handschrifterkennung mit einem herkenzer-Handle und einem Erkennungs Kontext als hrecocontext-handle. Eine Erkennungs Modul-dll (Dynamic-Link Library) kann Erkennungs Tools für mehr als eine Sprache implementieren.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: Herkenzer und hrecocontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345128"
---
# <a name="hrecognizer-and-hrecocontext"></a>Herkenzer und hrecocontext

Sie verweisen auf eine Handschrifterkennung mit einem [herkenzer](hrecognizer-handle.md) -Handle und einem Erkennungs Kontext als [hrecocontext](hrecocontext-handle.md) -handle.

Eine Erkennungs Modul-dll (Dynamic-Link Library) kann Erkennungs Tools für mehr als eine Sprache implementieren. Wenn dies der Fall ist, wird jede Sprache durch eine CLSID ausgewählt, die beim Erstellen des [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekts in der Anwendung übermittelt wird. Außerdem kann eine Erkennungs-DLL mehrere Erkennungs Handles erstellen, wenn Sie geladen wird, eine oder mehrere für jede erkannte Sprache.

Ein Erkennungs Kontext wird erstellt, um das Ereignis zu repräsentieren, das ein bestimmtes frei Hand Element erkennt. Wenn der Kontext erstellt wird, wird das zugehörige Erkennungs Objekt Handle an die Funktion " [**featecontext**](/windows/desktop/api/recapis/nf-recapis-createcontext) " übergeben. Dadurch wird die Sprache dem Erkennungs Kontext zugeordnet.

Ein Erkennungs Kontext kann die Erkennung sämtlicher frei Hand Eingaben im Textkörper einer e-Mail, das frei Handzeichen eines einzelnen Felds innerhalb einer Anwendung oder eine einzelne Textzeile darstellen, die im Tablet PC-Eingabe Panel geschrieben ist. Die Menge an frei Hand Eingaben in einem einzelnen Erkennungs Kontext kann von einem einzelnen Strich zu einer ganzen Seite oder mehr abweichen.

Der Erkennungs Kontext wird durch die folgenden Einstellungen definiert:

-   Das Erkennungs Handbuch.
-   Alle Faktoide.
-   Alle Flags.
-   Der Text Kontext.
-   Eine beliebige Wort Liste.
-   Der AutoComplete-Zeichenmodus.

Das Handle für den Erkennungs Kontext wird an alle Funktionen, die diese Einstellungen verwenden, übermittelt. Durch Ändern einer Einstellung wird der Erkennungs Kontext geändert.

Die Anwendung kann mehrere Kontexte verwenden, um frei Hand Eingaben aus verschiedenen Teilen des Bildschirms zu erkennen. Ein einzelner Kontext kann mehrere Textzeilen erkennen. Ein einzelner Kontext kann jedoch zwei Absätze, die nebeneinander geschrieben wurden, nicht gleichzeitig verarbeiten, z. b. mehrere Spalten in einem Zeitungsartikel.

Um neue frei Hand Eingaben zu erkennen, erstellen Sie einen neuen Kontext. Verwenden Sie als Alternative die [**clonecontext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) -Funktion, um eine Kopie eines Kontexts zu erstellen, der keine frei Hand Eingaben und Ergebnisse enthält, oder die [**resetcontext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) -Funktion, um einen Kontext der frei Hand Eingaben und Ergebnisse zu löschen. Mit diesen Ansätzen kann eine Ink-Anwendung einen Kontext wieder verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Setguide-Funktion**](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[**Getguide-Funktion**](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[**Setfaktoid-Funktion**](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[**SetFlags-Funktion**](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[**"Stenabledunicoderanges"-Funktion**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[**GetEnabledUnicodeRanges-Funktion**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[**Setcacmode-Funktion**](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[**Settextcontext-Funktion**](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[**Setwordlist-Funktion**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



