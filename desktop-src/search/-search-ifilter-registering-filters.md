---
description: Der Filter Handler muss registriert werden. Sie können auch einen vorhandenen Filter Handler für eine angegebene Dateinamenerweiterung entweder über die Registrierung oder mithilfe der iloadfilter-Schnittstelle suchen.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Registrieren von Filter Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128565"
---
# <a name="registering-filter-handlers"></a>Registrieren von Filter Handlern

Der Filter Handler muss registriert werden. Sie können auch einen vorhandenen Filter Handler für eine angegebene Dateinamenerweiterung entweder über die Registrierung oder mithilfe der [**iloadfilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) -Schnittstelle suchen.

Dieses Thema ist wie folgt organisiert:

- [Registrieren von Filter Handlern für Windows Search](#registering-filter-handlers)
  - [Veralteter Ansatz zum Registrieren von Filter Handlern](#obsolete-approach-for-registering-filters-handlers)
- [Ersetzen von vorhandenen Filter Handlern](#replacing-existing-filter-handlers)
- [Suchen eines Filter Handlers für eine bestimmte Dateierweiterung](#finding-a-filter-handler-for-a-given-file-extension)
- [Weitere Ressourcen](#additional-resources)
- [Zugehörige Themen](#related-topics)

> [!NOTE]  
> Ein Filter Handler ist eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle.

## <a name="registering-filters-handlers-for-windows-search"></a>Registrieren von Filter Handlern für Windows Search

Die GUIDs, die Sie zum Registrieren eines neuen Protokoll Handlers oder zum Suchen eines vorhandenen Protokoll Handlers benötigen, sind in der folgenden Tabelle aufgeführt.

| GUID                                     | Benutzer oder Anwendung definiert | BESCHREIBUNG                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| **89bcb740-6119-101A-bcb7-00dd010655af** | Application                 | Der GUID der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle ist eine Konstante für den Registrierungsschlüssel für alle Filter Handler. |
| **{Persistenthandlerguid}**              | Benutzer                        | Dies ist die GUID für den persistenten Handler.                                                              |
| **{Filterhandlerclsid}**                 | Benutzer                        | Dies ist der Klassen Bezeichner (CLSID) für den Filter Handler.                                              |
| **{Applicationguid}**                    | Benutzer                        | Dies ist eine zwischen (aggregierte) GUID.                                                                |

Filter Handler müssen auf dem lokalen HKEY-Computer registriert werden, \_ \_ da SearchFilterHost.exe unter dem System Konto ausgeführt wird und daher nicht auf die Registrierungsschlüssel für den aktuellen HKEY- \_ \_ Benutzer für den angemeldeten Benutzer zugreifen kann. Außerdem muss die Gruppe "Benutzer" über Lese-und Ausführungs Berechtigungen für die Datei "Filter Handler. dll" verfügen, da SearchFilterHost.exe alle Administratorrechte entfernt und nur nicht Administratorrechte zulässt. Da sich der Standard Speicherort von Visual Studio im Verzeichnis des aktuellen Benutzers befindet und keine Leseberechtigungen für die Benutzergruppe erteilt, müssen Sie entweder die DLL-Datei verschieben oder die ACLs ändern, um SearchFilterHost.exe Zugriff zuzulassen.

Wenn Sie einen neuen Filter Handler registrieren, empfiehlt es sich, einen beschreibenden Namen zu verwenden, z. b. html-IFilter.

**So registrieren Sie den neuen Filter Handler:**

1. Geben Sie die Erweiterung und die persistente handlerguid an, von der der Filter Handler verwendet wird:

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. Registrieren Sie den Filter Handler mit den folgenden Schlüsseln und Werten:

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a>Veralteter Ansatz zum Registrieren von Filter Handlern

Diese Vorgehensweise wird nicht für die Verwendung empfohlen. Filter können für eine CLSID registriert werden, die eine Component Object Model (com)-Klasse und/oder für eine Dateinamenerweiterung darstellt. Sie können beide Filter registrieren, wenn Sie einen Filter Handler für eine Klasse registrieren müssen, und einen anderen Filter Handler für eine Dateinamenerweiterung innerhalb der Klasse. Beachten Sie, dass ein für eine Dateinamenerweiterung registrierter Filter Handler Vorrang vor einem Filter Handler für eine CLSID hat.

Diese Einträge sind OLE-Standard Registrierungseinträge bis einschließlich des Eintrags für die Klassen- **CLSID \\ {applicationguid}**. Die dll-sample.dll implementiert das Verhalten für das Ausführen von Objekten für die txt-Klasse. Beachten Sie den zusätzlichen Eintrag PersistentHandler. Dieser Eintrag gibt die Klasse an, die für das Broker von Anforderungen an die persistenten Objekte der Beispiel Klasse zuständig ist. Der Eintrag unter **persistentaddinsregistered** identifiziert die für die Schnittstelle mit dem Namen **89bcb740-6119-101A-bcb7-00dd010655af**(IID \_ IFilter) Verantwortliche Implementierung. Die Klasse, die **IID \_ IFilter** implementiert, verfügt über Standard-OLE-Registrierungseinträge. Die InprocServer32-dll wird über den OLE-Standardmechanismus geladen.

Windows Search beobachtet das Thread Modell, das für den Filter Handler angegeben ist. Wenn das Threading Modell auf **beide** festgelegt ist, muss der Filter Handler Thread sicher sein. Wenn Sie andernfalls nicht Thread sicher ist, geben Sie **Apartment** an. Beachten Sie, dass Filter Handler immer Thread sicher sein sollten.

Die folgenden Beispiel Registrierungseinträge gelten für einen Filter Handler, der für eine Klassen-und Dateinamenerweiterung registriert ist. **{Persistenthandlerguid}** und **{filterhandlerclsid}** werden als Variablen zum Angeben von Werten verwendet, die vom Ersteller des Filter Handlers angegeben werden müssen. Die Werte sind vom Typ reg \_ SZ.

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a>Ersetzen von vorhandenen Filter Handlern

Es wird empfohlen, die integrierten Filter Handler nicht für allgemeine Dateitypen wie txt, doc, HTML,. URL usw. zu ersetzen, da dies unerwünschte Auswirkungen auf andere Systemkomponenten haben kann. Das Indizieren von e-Mail-Nachrichtentext hängt z. b. von den Filter Handlern. txt,. html und RTF ab.

Wenn ein neuer Filter Handler für einen Dateityp als Ersatz für eine vorhandene Filter Registrierung installiert wird, sollte der Installer die aktuelle Registrierung speichern und wiederherstellen, wenn der neue Filter Handler deinstalliert wird. Es gibt keinen Mechanismus zum Verketten von Filtern. Daher ist der neue Filter Handler für die Replikation aller notwendigen Funktionen des alten Filters verantwortlich.

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a>Suchen eines Filter Handlers für eine bestimmte Dateierweiterung

Sie können die [**iloadfilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) -Schnittstelle verwenden, um einen Filter Handler für eine angegebene Dateinamenerweiterung zu suchen. Die folgenden Beispiel Registrierungseinträge veranschaulichen, wie dies für HTML-Dateien durchzuführen ist. In diesem Beispiel wird der Filter Handler für HTML-Dokumente nlhtml.dll. Die Werte sind vom Typ reg \_ SZ.

**So finden Sie den Filter Handler für eine bestimmte Dateinamenerweiterung:**

1. Überprüfen Sie, ob die Erweiterung für den Typ der gefilterten Dateien über einen permanenten Handler verfügt, der im Registrierungs Eintrag \\ HKEY \_ local \_ Machine \\ \\ Classes Software Classes. Extension registriert ist. Wenn dies der Fall ist, lassen Sie diesen Schlüssel {persistenthandlerguid}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. Wenn kein persistenter Handler für die Erweiterung registriert ist, suchen Sie nach der CLSID, die dem Dokumenttyp im Registrierungs Eintrag \\ HKEY \_ local \_ Machine- \\ Software \\ Klassen zugeordnet ist. Übernehmen Sie diesen Schlüssel {applicationguid}. Legen Sie dann fest, ob ein permanenter Handler für die CLSID registriert ist: Suchen Sie mithilfe von {applicationguid} den permanenten Handler für den \\ \_ Eintrag " \_ \\ \\ \\ CLSID \\ {applicationguid}" der HKEY Local Machine Classes. Lassen Sie diesen Schlüssel {persistenthandlerguid}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. Bestimmen Sie die GUID des permanenten Handlers: Verwenden Sie {persistenthandlerguid}, um die persistente handlerguid für den Dokumenttyp zu suchen. Der Wert unter dem Registrierungs Eintrag HKEY \_ local \_ Machine \\ \\ Classes \\ CLSID \\ {persistenthandlerguid} \\ persistentaddinsregistered \\ 89bcb740-6119-101A-bcb7-00dd010655af ergibt die persistente handlerguid für diesen Dokumenttyp. Lassen Sie den Schlüssel {filterhandlerclsid}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Bestimmen des Filter Handlers: mithilfe von {filterhandlerclsid}, der im vorherigen Schritt ermittelt wurde, finden Sie den Filter Handler unter dem Eintrag \\ HKEY \_ local \_ Machine \\ \\ Classes \\ CLSID \\ {filterhandlerclsid} \\ InProcServer32. In diesem Beispiel ist der Name des beschreibenden Filter Handlers der HTML-IFilter.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a>Weitere Ressourcen

- Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Basisklasse für die Implementierung der **IFilter** -Schnittstelle erstellt wird.
- Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
- Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).
- Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".

## <a name="related-topics"></a>Zugehörige Themen

[Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)

[Informationen zu Filter Handlern in Windows Search](-search-ifilter-about.md)

[Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)

[Zurückgeben von Eigenschaften aus einem Filter Handler](-search-ifilter-property-filtering.md)

[Filtern von Handlern, die mit Windows ausgeliefert werden](-search-ifilter-implementations.md)

[Implementieren von Filter Handlern in Windows Search](-search-ifilter-constructing-filters.md)

[Testen von Filter Handlern](-search-ifilter-testing-filters.md)
