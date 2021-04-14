---
description: MUI ermöglicht es Ihren Anwendungen, Benutzeroberflächen Sprachen auf zwei Arten zu verwalten.
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: Sprach Verwaltung in der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852fe20d3edb9795c2c2a9d3ec45c1e8ffe053ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393785"
---
# <a name="user-interface-language-management"></a>Sprach Verwaltung in der Benutzeroberfläche

MUI ermöglicht es Ihren Anwendungen, Benutzeroberflächen Sprachen auf zwei Arten zu verwalten. Eine Anwendung kann einen einfachen Ansatz für die sprach Verwaltung verwenden, indem Sie die Spracheinstellungen für das Betriebssystem standardmäßig verwendet. Alternativ kann die Anwendung auch Ihre eigenen Sprachen unterstützen, von denen der Benutzer auswählen kann. Die MUI-API ermöglicht der Anwendung auch den direkten Zugriff auf Sprachen und sprach Listen, die vom Betriebssystem unterstützt werden und vom Ressourcen Lader verwaltet werden. Im restlichen Teil dieses Themas werden die vom System unterstützten Sprachen und der sprach Fall Back Mechanismus definiert.

## <a name="languages-maintained-by-the-operating-system"></a>Vom Betriebs System verwalteten Sprachen

### <a name="system-default-ui-languageinstall-language"></a>System Standardbenutzer Oberflächen Sprache/Installationssprache

Die standardmäßige Benutzeroberflächen Sprache des Systems ist die Sprache der lokalisierten Version, die zum Einrichten von Windows verwendet wird. Alle Menüs, Dialogfelder, Fehlermeldungen und Hilfedateien werden in dieser Sprache dargestellt, es sei denn, der Benutzer wählt eine andere Sprache aus.

Unter Windows Vista und höher wird die Benutzeroberflächen Sprache des Systems standardmäßig als "Installationssprache" bezeichnet und spielt eine eingeschränkte Rolle. In den meisten Fällen wird Sie von den bevorzugten Benutzeroberflächen Sprachen des Systems abgelöst. In bestimmten Kontexten ist es jedoch sinnvoll, eine einzelne Installationssprache zu haben, die immer bekanntermaßen vollständig unterstützt wird.

Es ist keine MUI-Funktion verfügbar, um die Standardbenutzer Oberflächen Sprache des Systems festzulegen. Zum Abrufen dieser Sprache kann die Anwendung [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)aufrufen.

### <a name="system-ui-language"></a>Benutzeroberflächen Sprache des Systems

Das Betriebssystem definiert die Benutzeroberflächen Sprache des Systems als Benutzeroberflächen Sprache, die von einem Administrator auf der Registerkarte **erweitert** des Bereichs Regions-und Sprachoptionen in der Systemsteuerung festgelegt werden kann. Das Betriebssystem verwendet diese Sprache, wenn der aktuelle Benutzer keine bestimmten Spracheinstellungen vorgenommen hat oder wenn kein aktives Konto angemeldet ist. Die Sprache kann nur geändert werden, wenn mehr als eine Benutzeroberflächen Sprache auf dem Computer installiert ist.

> [!Note]  
> Das Betriebssystem muss für alle Benutzer und Dienste neu gestartet werden, um die Auswirkung der sprach Änderung anzuzeigen.

 

Es ist keine MUI-Funktion verfügbar, um die Benutzeroberflächen Sprache des Systems festzulegen. Zum Abrufen dieses Werts kann eine Anwendung, die auf Windows Vista und höher ausgerichtet ist, [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) aufrufen und die erste Sprache in der Liste der bevorzugten Benutzeroberflächen Sprachen des Systems erhalten. Anwendungen, die auf Betriebssysteme vor Windows Vista ausgerichtet sind, können [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) nicht verwenden. Sie sollten darauf basieren, dass die Benutzeroberflächen Sprache des Systems stets mit der Standardbenutzer Oberfläche des Systems identisch ist.

### <a name="user-ui-language"></a>Benutzeroberflächen Sprache

Die Benutzeroberflächen Sprache des Benutzers bestimmt die Sprache der Benutzeroberfläche, die für Menüs, Dialogfelder, Hilfedateien usw. verwendet wird. Sie kann vom aktuellen Benutzer auf der Registerkarte **Sprache** des Bereichs Regions-und Sprachoptionen in der Systemsteuerung festgelegt werden. Diese Sprache kann nur geändert werden, wenn mehr als eine Benutzeroberflächen Sprache auf dem Computer installiert ist. Beachten Sie, dass sich der Benutzer ab-und wieder anmelden muss, um die Auswirkung anzuzeigen. Ein multinationales Unternehmen möchte beispielsweise in allen Niederlassungen Windows bereitstellen. Das Unternehmen erstellt einen globalen Installations Auftrag, bei dem die englische Sprachversion von Windows auf allen Clients installiert wird, unabhängig vom Standort. Gleichzeitig werden bestimmte Sprachmodule installiert, abhängig von der Organisationseinheit, der ein Computer angehört. Wenn sich der Benutzer zum ersten Mal bei einem neu installierten Betriebssystem anmeldet, wird Windows als lokalisierte Version angezeigt.

Unter Windows Vista und höher ist die Benutzeroberflächen Sprache des Benutzers die erste Sprache in der Liste Benutzer bevorzugte UI-Sprachen. Beachten Sie, dass Fall Back Sprachen verwendet werden können, wenn bestimmte Ressourcen in dieser Sprache nicht verfügbar sind.

Bei Betriebssystemen vor Windows Vista ist die Benutzeroberflächen Sprache des Benutzers in der Regel mit der Benutzeroberflächen Sprache des Systems identisch. Für Windows MUI können sich die beiden Sprachen jedoch unterscheiden.

Zum Abrufen der Benutzeroberflächen Sprache des Benutzers kann eine Anwendung [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) oder [**getuserpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)aufrufen. Die Anwendung kann die Benutzeroberflächen Sprache des Benutzers nicht ändern, da Sie nicht festgelegt werden kann.

## <a name="language-lists-maintained-by-the-operating-system"></a>Vom Betriebs System verwaltet sprach Listen

### <a name="system-preferred-ui-languages-list"></a>Liste der bevorzugten Benutzeroberflächen Sprachen

Das Ressourcen Lade Modul verwaltet die Liste der bevorzugten Benutzeroberflächen Sprachen des Systems. In dieser Liste sind Sprachen enthalten, die vom Betriebssystem für seine eigenen Ressourcen bevorzugt werden, z. b. Menüs und Dialogfelder, Nachrichten, INF-Dateien und Hilfedateien. Die Liste besteht aus der Standardbenutzer Oberflächen Sprache des Systems und der Benutzeroberflächen Sprache des Systems sowie ihren Fallbacks. Eine Anwendung kann durch Aufrufen von [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)die bevorzugten Benutzeroberflächen Sprachen des Systems abrufen.

### <a name="user-preferred-ui-languages-list"></a>Benutzer bevorzugte UI-Sprachen Liste

Das Ressourcen Lade Modul verwendet eine bevorzugte Benutzeroberflächen Sprachen-Liste, die vom Benutzer bevorzugte Sprachen enthält. Das Ressourcen Lade Modul verwendet Ressourcen, die für einen bestimmten Anwendungs Thread in dieser Liste mit den Sprachen übereinstimmen, falls verfügbar. Diese Sprachen haben Vorrang vor allen Systemeinstellungen. Zum Abrufen von Benutzer bevorzugten Benutzeroberflächen Sprachen kann die Anwendung [**getuserpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)aufrufen.

### <a name="process-preferred-ui-languages-list"></a>Liste der bevorzugten Benutzeroberflächen Sprachen verarbeiten

Unter Windows Vista und höher verwaltet das Ressourcen Lade Modul eine Liste der bevorzugten Benutzeroberflächen Sprachen, die aus bis zu fünf gültigen Sprachen besteht, die von einem laufenden Prozess für eine MUI-Anwendung festgelegt werden. Die Sprachen können von der Anwendung mit einem Aufrufen von [**setprocesliniferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)festgelegt werden. Die Anwendung kann die Sprachen abrufen, indem Sie [**getprocesliniferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages)aufrufen.

### <a name="thread-preferred-ui-languages-list"></a>Liste der bevorzugten Thread Sprachen der Benutzeroberfläche

Unter Windows Vista und höher wird vom Ressourcen Lader eine Thread bevorzugte Liste der Benutzeroberflächen Sprachen verwendet, die aus bis zu fünf gültigen Sprachen besteht, die von einem Thread in einem laufenden Prozess für eine MUI-Anwendung festgelegt werden. Diese Sprachen werden verwendet, um die Sprachen der Anwendungs Benutzeroberfläche anzupassen und Sie von der Sprache des Betriebssystems zu unterscheiden. Die Liste der bevorzugten Threads in der Benutzeroberfläche des Threads basiert auf den bevorzugten Benutzeroberflächen Sprachen des Benutzers, den bevorzugten Benutzeroberflächen Sprachen des Benutzers und der standardmäßigen Benutzeroberflächen Sprache des Systems.

Um die bevorzugten Thread Sprachen der Benutzeroberfläche festzulegen, sollte die Anwendung [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)aufrufen. Um diese Sprachen abzurufen, ruft die Anwendung [**getthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)auf.

## <a name="neutral-language-representation"></a>Neutrale Sprachdarstellung

Eine neutrale Sprache wird ausschließlich als Sprache ohne Region oder Gebiets Schema dargestellt. Beispielsweise wird die neutrale Darstellung der Sprache Deutsch (Kanada), en-ca, als "en" dargestellt. Obwohl eine neutrale Sprache nicht den Aspekten einer Region oder eines Gebiets Schemas zugeordnet ist, können Sie Sie einem Ressourcen Satz zuordnen. In der Regel basiert eine neutrale Sprachressource auf der Verwendung in der am weitesten verbreiteten Region der Sprache.

Angenommen, ihre MUI-Anwendung lokalisiert die deutschen Sprachressourcen für Deutsch (Schweiz), dargestellt als de-ch und Deutsch (Österreich), dargestellt als de-at, während Sie einen vollständigen Satz von Ressourcen für Deutsch (Deutschland) aufbauen, der als de-de dargestellt wird. Sie müssen Entscheidungen für diese Anwendung treffen, wenn Sie die gesamten Ressourcen Dateien berücksichtigen. Wenn die Anwendung die de-de-Ressourcen als neutrale Sprachressourcen dupliziert, muss Sie eine Fall Back Sprache für das Ressourcen Lade Modul bereitstellen. Wenn das Lade Modul keine bestimmte sprachspezifische Ressourcen Datei für de-ch oder für de-at findet, greift es auf die sprach neutralen "de"-Ressourcen zurück. Diese Ressourcen sind höchstwahrscheinlich besser geeignet als Ressourcen für eine völlig andere Sprache, z. b. "Englisch (USA)", bei denen es sich um die einzigen anderen möglichen Fallbacks handelt.

Ein weiteres Beispiel ist, dass eine Anwendung in Belize überhaupt nicht lokalisiert werden kann. Die Unterstützung der Spracheinstellung Englisch (Belize), dargestellt als en-BZ, ermöglicht der Anwendung jedoch, auf "en"-Ressourcen zurückzugreifen.

## <a name="language-fallback-in-the-resource-loader"></a>Sprach Fallback im Ressourcen Lader

Windows Vista und höher ordnen Sie die Spracheinstellungen der Benutzeroberfläche in einer vom Ressourcen Lader verwendeten Liste von vordefinierten Fall Back Sprachen an. Zum bilden der Liste kombiniert das Betriebssystem mehrere Sprachen in der angezeigten Reihenfolge:

-   Thread bevorzugte UI-Sprachen, bestehend aus der Sprache der Thread Benutzeroberfläche und ihrer neutralen Form. Beispiele hierfür sind "fr-FR" für Französisch (Frankreich) und die neutrale Form "fr" und es-es für Spanisch (Spanien) und die neutrale Form "es".
-   Verarbeiten der bevorzugten Benutzeroberflächen Sprachen, bestehend aus der Sprache der Prozess Benutzeroberfläche und ihrer neutralen Form. Ein Beispiel hierfür ist de-de für Deutsch (Deutschland) und die neutrale Form "de".
-   Benutzeroberflächen Sprache des Benutzers und seine neutrale Form. Ein Beispiel ist ja-JP für Japanisch (Japan) und die neutrale Form "Ja".
-   Benutzeroberflächen Sprache des Systems und deren neutrale Form. Ein Beispiel hierfür ist, dass es für Italienisch (Italien) und seine neutrale Form "IT" ist.
    > [!Note]  
    > Diese Sprache ist nur in der Fall Back Liste enthalten, wenn die Benutzeroberflächen Sprache des Benutzers nicht festgelegt ist.

     

-   Standardmäßige Benutzeroberflächen Sprache des Systems und deren neutrales Formular. Ein Beispiel hierfür sind es-es für Spanisch (Spanien) und die neutrale Form "es".

Im folgenden wird die zusammengeführte Fall Back Liste gezeigt. Beachten Sie, dass die Duplizierung von Sprachen, z. b. "es-es" und "es", entfällt. Da im Beispiel die Benutzeroberflächen Sprache des Benutzers auf ja-JP festgelegt wird, wird die Benutzeroberflächen Sprache des Systems nicht in der zusammengeführten Fall Back Liste angezeigt.

fr-FR, Fr, es-es, es, de-de, de, ja-JP, ja

Beim Laden von Ressourcen für eine MUI-Anwendung versucht das Ressourcen Lader, eine der Dateien auszuwählen, die mit der Liste der bevorzugten Thread Sprachen der Benutzeroberfläche für den aktuell ausgewenden Anwendungs Thread übereinstimmen. Wenn das Ressourcen Lade Modul keine direkte Entsprechung zwischen einer ausgewählten Sprache und der ersten sprachspezifischen Ressource in der zusammengeführten Fall Back Liste findet, werden die nachfolgenden Sprachen in der Liste überprüft, bis ein akzeptabler Fall Back gefunden wird.

Wenn das Ressourcen Lade Modul keine benötigte Datei findet, muss es eine "garantierte gute" Fall Back Sprache verwenden. Bei der MUI-Ressourcen Technologie bestimmt das Ressourcen Lade Modul die Fall Back Sprache aus den bereitgestellten Ressourcen Konfigurationsdaten. Weitere Informationen finden Sie unter [MUI-Ressourcenverwaltung](mui-resource-management.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über mehrsprachige Benutzeroberfläche](about-multilingual-user-interface.md)
</dt> <dt>

[Gebiets Schemas und Sprachen](locales-and-languages.md)
</dt> <dt>

[NLS-Terminologie](nls-terminology.md)
</dt> </dl>

 

 



