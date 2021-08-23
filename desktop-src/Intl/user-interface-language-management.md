---
description: MIT DEM PROGRAMM KÖNNEN Ihre Anwendungen Benutzeroberflächensprachen auf zwei Arten verwalten.
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: Benutzeroberfläche Language Management
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aaf20ca6183109f81572eeb706673812fc988eca87ea2522f437eafd22774b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631840"
---
# <a name="user-interface-language-management"></a>Benutzeroberfläche Language Management

MIT DEM PROGRAMM KÖNNEN Ihre Anwendungen Benutzeroberflächensprachen auf zwei Arten verwalten. Eine Anwendung kann einen einfachen Ansatz für die Sprachverwaltung verwenden, indem standardmäßig die Spracheinstellungen des Betriebssystems verwendet werden. Alternativ kann die Anwendung ihre eigenen Sprachen unterstützen, aus denen der Benutzer auswählen kann. Die API FÜR DIE ERWEITERUNG ermöglicht Ihrer Anwendung auch den direkten Zugriff auf Sprachen und Sprachlisten, die vom Betriebssystem unterstützt und vom Ressourcenladeprogramm verwaltet werden. Im weiteren Verlauf dieses Themas werden die vom System unterstützten Sprachen und der Sprachfallbackmechanismus definiert.

## <a name="languages-maintained-by-the-operating-system"></a>Vom Betriebssystem aufrechterhaltene Sprachen

### <a name="system-default-ui-languageinstall-language"></a>Standardsprache der Benutzeroberfläche des Systems/Installationssprache

Die Standardsprache der Benutzeroberfläche des Systems ist die Sprache der lokalisierten Version, die zum Einrichten Windows verwendet wird. Alle Menüs, Dialogfelder, Fehlermeldungen und Hilfedateien werden in dieser Sprache dargestellt, es sei denn, der Benutzer wählt eine andere Sprache aus.

Auf Windows Vista und höher wird die Standardsprache der Benutzeroberfläche des Systems als "Installationssprache" bezeichnet und spielt eine eingeschränktere Rolle. Für die meisten Zwecke wird sie durch die vom System bevorzugten Benutzeroberflächensprachen ersetzt. In bestimmten Kontexten ist es jedoch hilfreich, eine einzelne Installationssprache zu verwenden, die immer als vollständig unterstützt bekannt ist.

Zum Festlegen der Standardsprache für die Benutzeroberfläche des Systems ist keine FUNKTION VOMRverfügbar. Um diese Sprache abzurufen, kann die Anwendung [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)aufrufen.

### <a name="system-ui-language"></a>Sprache der System-UI

Das Betriebssystem definiert die Benutzeroberflächensprache des Systems als Sprache für die Benutzeroberfläche, die von einem Administrator auf der Registerkarte **Erweitert** des Regions- und Sprachoptionenteils von Systemsteuerung festgelegt werden kann. Das Betriebssystem verwendet diese Sprache, wenn der aktuelle Benutzer keine bestimmten Spracheinstellungen vorgenommen hat oder wenn kein aktives Konto angemeldet ist. Die Sprache kann nur geändert werden, wenn mehr als eine Benutzeroberflächensprache auf dem Computer installiert ist.

> [!Note]  
> Das Betriebssystem muss neu gestartet werden, damit alle Benutzer und Dienste die Auswirkungen der Sprachänderung sehen können.

 

Zum Festlegen der Benutzeroberflächensprache des Systems ist keine FUNKTION VOM VERFÜGBAR. Um diesen Wert abzurufen, kann eine Anwendung, die auf Windows Vista und höher abzielt, [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) aufrufen und die erste Sprache in der Liste der bevorzugten Benutzeroberflächensprachen des Systems abrufen. Anwendungen, die auf Betriebssysteme vor Windows Vista ausgerichtet sind, können [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) nicht verwenden und sollten auf der Annahme basieren, dass die Benutzeroberflächensprache des Systems immer mit der Standardsprache der Benutzeroberfläche des Systems identisch ist.

### <a name="user-ui-language"></a>Benutzer-UI-Sprache

Die Benutzeroberflächensprache bestimmt die Sprache der Benutzeroberfläche, die für Menüs, Dialogfelder, Hilfedateien usw. verwendet wird. Sie kann vom aktuellen Benutzer auf der Registerkarte **Sprache** des Regions- und Sprachoptionenteils von Systemsteuerung festgelegt werden. Diese Sprache kann nur geändert werden, wenn mehr als eine Benutzeroberflächensprache auf dem Computer installiert ist. Beachten Sie, dass sich der Benutzer abmelden und dann wieder anmelden muss, um die Auswirkung zu sehen. Beispielsweise möchte ein multinationales Unternehmen Windows in allen Niederlassungen bereitstellen. Das Unternehmen erstellt einen globalen Installationsauftrag, bei dem die englischsprachige Version von Windows unabhängig vom Standort auf allen Clients installiert wird. Gleichzeitig werden bestimmte Sprachmodule installiert, abhängig von der Organisationseinheit, der ein Computer angehört. Wenn sich der Benutzer zum ersten Mal bei einem neu installierten Betriebssystem anmeldet, wird Windows als lokalisierte Version angezeigt.

Auf Windows Vista und höher ist die Benutzeroberflächensprache die erste Sprache in der Liste der bevorzugten Benutzeroberflächensprachen. Beachten Sie, dass Fallbacksprachen verwendet werden können, wenn bestimmte Ressourcen in dieser Sprache nicht verfügbar sind.

Bei Betriebssystemen vor Windows Vista entspricht die Benutzeroberflächensprache in der Regel der Standardsprache der Benutzeroberfläche des Systems. Für Windows JEDOCH KÖNNEN sich die beiden Sprachen unterscheiden.

Um die Benutzeroberflächensprache abzurufen, kann eine Anwendung [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) oder [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)aufrufen. Die Benutzeroberflächensprache kann von der Anwendung nicht geändert werden, da keine Funktion zum Festlegen vorhanden ist.

## <a name="language-lists-maintained-by-the-operating-system"></a>Vom Betriebssystem gepflegte Sprachlisten

### <a name="system-preferred-ui-languages-list"></a>Liste der bevorzugten Benutzeroberflächensprachen des Systems

Das Ressourcenladeprogramm verwaltet eine Liste der vom System bevorzugten UI-Sprachen. In dieser Liste sind Sprachen enthalten, die vom Betriebssystem für eigene Ressourcen bevorzugt werden, z. B. Menüs und Dialoge, Nachrichten, INF-Dateien und Hilfedateien. Die Liste besteht aus der Standardsprache der Benutzeroberfläche des Systems, der Benutzeroberflächensprache des Systems und ihren Fallbacks. Eine Anwendung kann vom System bevorzugte Ui-Sprachen abrufen, indem [**sie GetSystemPreferredUILanguages aufruft.**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)

### <a name="user-preferred-ui-languages-list"></a>Liste der bevorzugten Benutzeroberflächensprachen

Das Ressourcenladeprogramm verwendet eine Vom Benutzer bevorzugte Ui-Sprachenliste, die sprachen enthält, die der Benutzer bevorzugt. Das Ressourcenladeprogramm verwendet Ressourcen, die sprachenübereinstimmungen, sofern verfügbar, für einen bestimmten Anwendungsthread aus dieser Liste. Diese Sprachen haben Vorrang vor allen Systemeinstellungen. Um vom Benutzer bevorzugte Benutzeroberflächensprachen abzurufen, kann Ihre Anwendung [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)aufrufen.

### <a name="process-preferred-ui-languages-list"></a>Process Preferred UI Languages List

Auf Windows Vista und höher verwaltet das Ressourcenladeprogramm eine Liste der bevorzugten Ui-Sprachen für den Prozess, die aus bis zu fünf gültigen Sprachen besteht, die von einem laufenden Prozess für eine VISTA-Anwendung festgelegt werden. Die Sprachen können von der Anwendung mit einem Aufruf von [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)festgelegt werden. Die Anwendung kann die Sprachen abrufen, indem [**Sie GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages)aufrufen.

### <a name="thread-preferred-ui-languages-list"></a>Liste der bevorzugten UI-Sprachen für Threads

Auf Windows Vista und höher verwendet das Ressourcenladeprogramm eine Thread-BEVORZUGTE UI-Sprachenliste, die aus bis zu fünf gültigen Sprachen besteht, die von einem Thread in einem laufenden Prozess für eine VISTA-Anwendung festgelegt werden. Diese Sprachen werden verwendet, um die Sprachen der Benutzeroberfläche der Anwendung anzupassen und sie von der Sprache des Betriebssystems abzuweichen. Die Liste der bevorzugten Ui-Sprachen des Threads basiert auf den vom Benutzer bevorzugten Benutzeroberflächensprachen, den vom System bevorzugten Ui-Sprachen und der Standardsprache der Benutzeroberfläche des Systems.

Um die bevorzugten Ui-Sprachen für den Thread festzulegen, sollte die Anwendung [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)aufrufen. Um diese Sprachen abzurufen, ruft die Anwendung [**GetThreadPreferredUILanguages auf.**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)

## <a name="neutral-language-representation"></a>Neutrale Sprachdarstellung

Eine neutrale Sprache wird als sprache allein dargestellt, ohne Region oder Gebietsschema. Beispielsweise wird die neutrale Darstellung der englischen Sprache (Kanada) en-CA als "en" dargestellt. Obwohl eine neutrale Sprache nicht den Aspekten einer Region oder eines Gebietsschemas zugeordnet ist, können Sie sie einem Ressourcensatz zuordnen. In der Regel basiert eine neutrale Sprachressource auf der Verwendung in der am häufigsten verwendeten Region für die Sprache.

Nehmen wir zur Veranschaulichung an, dass Ihre ANWENDUNG FÜR DIE DEUTSCHEN RESSOURCEN für Deutsch (Schweiz) lokalisiert, die als de-CH und Deutsch (Schweiz) als de-AT dargestellt werden, während sie einen vollständigen Satz von Ressourcen für Deutsch (Deutschland) erstellen, das als de-DE dargestellt wird. Sie müssen Entscheidungen für diese Anwendung unter Berücksichtigung der gesamten Ressourcendateien treffen. Wenn die Anwendung die De-DE-Ressourcen als neutrale Sprachressourcen dupliziert, muss sie eine Fallbacksprache für das Ressourcenladeprogramm bereitstellen. Wenn das Ladeprogramm keine bestimmte sprachspezifische Ressourcendatei für de-CH oder de-AT findet, greift es auf die sprachneutralen "de"-Ressourcen zurück. Diese Ressourcen sind wahrscheinlich besser geeignet als Ressourcen für eine völlig andere Sprache, z. B. Englisch (USA), die einzigen anderen möglichen Fallbacks.

Ein weiteres Beispiel ist, dass eine Anwendung für Dies überhaupt nicht lokalisiert wird. Durch die Unterstützung einer Sprachpräferenz für Englisch (), die als en-BZ dargestellt wird, kann die Anwendung jedoch auf "en"-Ressourcen zurückgreifen.

## <a name="language-fallback-in-the-resource-loader"></a>Sprachfallback im Ressourcenladeprogramm

Windows Vista und höher ordnen die Spracheinstellungen der Benutzeroberfläche in einer vordefinierten Fallbacksprachliste an, die vom Ressourcenladeprogramm verwendet wird. Um die Liste zu bilden, kombiniert das Betriebssystem mehrere Sprachen in der gezeigten Reihenfolge:

-   Bevorzugte Sprachen der Threadbenutzeroberfläche, die aus der Sprache der Threadbenutzeroberfläche und ihrer neutralen Form bestehen. Beispiele hierfür sind fr-FR für Französisch (Frankreich) und die neutrale Form "fr" und es-ES für Spanisch (Spanien) und die neutrale Form "es".
-   Verarbeiten Sie bevorzugte Benutzeroberflächensprachen, die aus der Sprache der Prozessbenutzeroberfläche und ihrer neutralen Form bestehen. Ein Beispiel ist de-DE für Deutsch (Deutschland) und seine neutrale Form "de".
-   Benutzeroberflächensprache und ihre neutrale Form. Ein Beispiel ist ja-JP für Japanisch (Japan) und seine neutrale Form "ja".
-   Sprache der System-Benutzeroberfläche und ihre neutrale Form. Ein Beispiel hierfür ist it-IT für Italienisch (Italienisch) und seine neutrale Form "it".
    > [!Note]  
    > Diese Sprache ist nur in der Fallbackliste enthalten, wenn die Benutzeroberflächensprache nicht festgelegt ist.

     

-   Standardsprache der Benutzeroberfläche des Systems und ihre neutrale Form. Ein Beispiel hierfür ist es-ES für Spanisch (Spanien) und seine neutrale Form "es".

Im Folgenden wird die zusammengeführte Fallbackliste angezeigt. Beachten Sie, dass die Duplizierung von Sprachen, z. B. es-ES und es, beseitigt wird. Da im Beispiel die Benutzeroberflächensprache auf ja-JP festgelegt wird, wird die Sprache der Systembenutzeroberfläche nicht in der zusammengeführten Fallbackliste angezeigt.

fr-FR, fr, es-ES, es, de-DE, de, ja-JP, ja

Beim Laden von Ressourcen für eine TRIES-Anwendung versucht das Ressourcenladeprogramm, eine der Dateien auszuwählen, die der Liste der bevorzugten UI-Sprachen für den aktuell ausgeführten Anwendungsthread entsprechen. Wenn das Ressourcenladeprogramm keine direkte Übereinstimmung zwischen einer ausgewählten Sprache und der ersten sprachspezifischen Ressource in der zusammengeführten Fallbackliste finden kann, überprüft es die nachfolgenden Sprachen in der Liste, bis ein akzeptabler Fallback gefunden wird.

Wenn das Ressourcenladeprogramm keine Datei findet, die es benötigt, muss es eine "garantiert gute" Fallbacksprache verwenden. Für die TECHNOLOGY DER RESSOURCE bestimmt das Ressourcenladeprogramm die Fallbacksprache aus den bereitgestellten Ressourcenkonfigurationsdaten. Weitere Informationen finden Sie unter [DER RESSOURCENverwaltung](mui-resource-management.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu mehrsprachige Benutzeroberfläche](about-multilingual-user-interface.md)
</dt> <dt>

[Gebietsschemas und Sprachen](locales-and-languages.md)
</dt> <dt>

[NLS-Terminologie](nls-terminology.md)
</dt> </dl>

 

 



