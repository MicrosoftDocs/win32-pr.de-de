---
title: Implementieren eines Protokoll Handlers für WDS
description: Zum Erstellen eines Protokoll Handlers gehört das Implementieren von isearchprotocol zum Verwalten von urlaccessor-Objekten, iurlaccessor zum Generieren von Metadaten über und das identifizieren geeigneter Filter für Elemente im Datenspeicher, iprotocolhandlersite zum Instanziieren eines searchprotocol-Objekts und identifizieren geeigneter Filter, und ifilterto filtert proprietäre Dateien oder hierarchisch gespeicherte Dateien.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101538"
---
# <a name="implementing-a-protocol-handler-for-wds"></a>Implementieren eines Protokoll Handlers für WDS

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Das Erstellen eines Protokoll Handlers umfasst das Implementieren von [**isearchprotocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) zum Verwalten von urlaccessor-Objekten, [**iurlaccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) zum Generieren von Metadaten über und das Ermitteln geeigneter Filter für Elemente im Datenspeicher, iprotocolhandlersite zum Instanziieren eines searchprotocol-Objekts und identifizieren geeigneter Filter und [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)zum Filtern von proprietären Dateien oder zum Auflisten und Filtern hierarchischer Dateien. Der Protokollhandler muss einen Multithread aufweisen.

Diese Abschnitte enthalten die folgenden Themen:

-   [Hinweis zu URLs](#note-on-urls)
-   [Protokollhandlerschnittstellen](#protocol-handler-interfaces)
-   [IFilters für Container](#ifilters-for-containers)
-   [Hinzufügen von protokollhandleroptionen](#adding-protocol-handler-options-functionality)
    -   [Isearchprotocoloptions](#isearchprotocoloptions)
-   [Zugehörige Themen](#related-topics)

## <a name="note-on-urls"></a>Hinweis zu URLs

Die Microsoft Windows-Desktop Suche (WDS) verwendet URLs, um Elemente in einem Dateisystem, in einem Daten bankähnlichen Speicher oder im Web eindeutig zu identifizieren. Eine URL, die einen Einstiegs Knoten definiert, wird als Startseite bezeichnet. WDS beginnt an dieser Startseite und rekursiv den Datenspeicher durch Crawlen. Die typische URL-Struktur lautet wie folgt:

`protocol://host/path/name.extension`

> [!Note]
>
> Wenn Sie einen neuen Datenspeicher hinzufügen möchten, müssen Sie einen Namen auswählen, um ihn zu identifizieren, der nicht mit aktuellen Konflikten in Konflikt steht. Diese Benennungs Konvention wird empfohlen: CompanyName. Scheme.

 

## <a name="protocol-handler-interfaces"></a>Protokollhandlerschnittstellen

**Isearchprotocol**

Die [**isearchprotocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) -Schnittstelle ruft urlaccessor-Objekte auf, initialisiert und verwaltet Sie. Weitere Informationen zum Implementieren der isearchprotocol-Schnittstelle finden Sie unter **isearchprotocol Interface Reference**.

**Iurlaccessor**

Für eine angegebene URL generiert die [**iurlaccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) -Schnittstelle Metadaten über die Standortstruktur sowie enthaltene Elemente und bindet diese Elemente an einen Filter. Das **iurlaccessor** -Objekt wird von einem searchprotocol-Objekt instanziiert und initialisiert. Sie können jedoch auch eine interne Initialisierungs Methode implementieren, damit Ihr **iurlaccessor** -Objekt Initialisierungs Aufgaben ausführen kann, die für den Protokollhandler spezifisch sind, z. b. das Überprüfen der URL für ein Element, auf das zugegriffen wird, oder das Überprüfen der Uhrzeit der letzten Änderung, um zu bestimmen, ob eine Datei in der aktuellen durch Forstung

> [!Note]
>
> Geänderte Zeiten für Verzeichnisse werden ignoriert. Das [**iurlaccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) -Objekt muss die untergeordneten Objekte auflisten, um zu bestimmen, ob Änderungen oder Löschungen vorhanden sind.

 

Ein Großteil des Entwurfs des **urlaccessor** -Objekts ist davon abhängig, ob die Struktur hierarchisch oder Links basiert ist. Bei hierarchischen Daten speichern muss das **urlaccessor** -Objekt einen Filter finden, der ihren Inhalt auflisten kann. Ein weiterer Unterschied zwischen hierarchischen und Link basierten Protokoll Handlern ist die Verwendung der IsDirectory-Methode. In Link basierten Protokoll Handlern sollte diese Methode den Wert S false zurückgeben \_ . Hierarchische Protokollhandler müssen für Container den Wert S OK zurückgeben \_ .

Weitere Anweisungen zum Implementieren einer [**iurlaccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) -Schnittstelle finden Sie unter [**iurlaccessor Interface**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) Reference.

**Iprotocolhandlersite**

Diese Schnittstelle wird verwendet, um ein **searchprotocol** -Objekt zu instanziieren und das **urlaccessor** -Objekt mit einem geeigneten Filter für eine angegebene Klassen-ID (CLSID) bereitzustellen.

## <a name="ifilters-for-containers"></a>IFilters für Container

Wenn Sie einen hierarchischen Protokollhandler implementieren, müssen Sie eine [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Container Komponente implementieren, die URLs auflistet, die Container oder Ordner darstellen. Der enumerationsprozess ist eine Schleife durch die **GetChunk** -Methode und die **GetValue** -Methode der IFilter-Schnittstelle, die eine Liste von URLs zurückgeben, die jedes Element im Container darstellen.

Zuerst gibt **GetChunk** eine Vollversion mit dem Eigenschaften Satz Gather \_ -propset zurück und eine der folgenden:

-   PID \_ gthr \_ dirlink, die URL zu dem Element ohne den Zeitpunkt der letzten Änderung, oder
-   PID \_ gthr \_ dirlink \_ with \_ Time, die URL zusammen mit dem Zeitpunkt der letzten Änderung

Der Eigenschafts Satz-GUID für das Gather- \_ propset lautet 0b63e343-9ccc-11D0-bcdb-00805f ccce04. Die PROPSPEC-Eigenschaft ist entweder PID \_ gthr \_ dirlink = 2 oder PID \_ gthr \_ dirlink \_ mit \_ Time = 12 Decimal.

Die Rückgabe \_ von PID gthr \_ dirlink \_ mit \_ Zeit ist effizienter, da der Indexer sofort ermitteln kann, ob das Element indiziert werden muss, ohne die Methoden isearchprotocol->createurlaccessor () und iurlaccessor->getLastModified () aufzurufende.

Anschließend gibt **GetValue** eine PROPVARIANT für die URL (und die Uhrzeit der letzten Änderung) wie folgt zurück:

-   VT \_ LPWSTR, die URL des untergeordneten Elements oder
-   Vektor der URL, auf die eine FILETIME folgt.

Der folgende Beispielcode veranschaulicht, wie die richtige PID \_ gthr \_ dirlink \_ mit \_ Zeit erstellt wird.

> [!Note]
>
> **Dieser Code und diese Informationen werden "wie immer" bereitgestellt, ohne jegliche Gewährleistungen jeglicher Art, entweder ausgedrückt oder impliziert, einschließlich, aber nicht beschränkt auf die impliziten Gewährleistungen der Handels Üblichkeit und/oder Eignung für einen bestimmten Zweck.**
>
> Copyright (C) Microsoft. Alle Rechte vorbehalten.

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]
>
> Eine [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Container Komponente sollte immer alle untergeordneten URLs auflisten, auch wenn sich die untergeordneten URLs nicht geändert haben, da der Indexer Löschungen durch den enumerationsprozess erkennt. Wenn die Datums Ausgabe in einem dir- \_ Link \_ mit \_ der Zeit anzeigt, dass die Daten nicht geändert wurden, aktualisiert der Indexer nicht die Daten für diese URL.

 

Die physische URL ist die URL, die vom **urlaccessor** -Objekt verarbeitet wird. Wenn der Filter keine benutzerfreundliche Display URL ausgibt, zeigt WDS die physische URL für den Benutzer als Teil der Suchergebnisse an. Das WDS-Schema enthält zwei Eigenschaften, mit denen gesteuert werden kann, was für den Endbenutzer angezeigt wird, wie in der folgenden Tabelle dargestellt.



| GUID                                 | PROPSPEC      | BESCHREIBUNG                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DisplayFolder | Ordner Pfad, der dem Benutzer in den Suchergebnissen angezeigt wird |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | FolderName    | Anzeige Name des übergeordneten Ordners                   |



 

Wenn Ihr Code keinen DisplayFolder oder FolderName ausgibt, werden diese Werte aus der displayurl berechnet. Schrägstriche in der URL bezeichnen Container innerhalb des Stores oder Dateisystems.

## <a name="adding-protocol-handler-options-functionality"></a>Hinzufügen von protokollhandleroptionen

Damit der Protokollhandler über eine Standard Startseite (und eine Eingabe Knoten-URL) verfügt, müssen Sie die **isearchprotocoloptions** -Schnittstelle implementieren. In zukünftigen Versionen von WDS stellt diese Schnittstelle dem Dialogfeld "Optionen" Hooks für eine verbesserte Benutzeroberfläche bereit. Diese Schnittstelle bietet die folgenden Funktionen:

-   Bestimmt, ob die Anforderungen für den Protokollhandler erfüllt sind. Der Speicher des Protokoll Handlers benötigt z. b. möglicherweise Zugriff auf eine bestimmte Anwendung, um die Daten der Anwendung ordnungsgemäß zu indizieren, aber diese Anwendung ist nicht verfügbar.
-   Gibt die Mindestanforderungen an, die der Protokollhandler für die Verarbeitung eines Elements benötigt. Anforderungen können in einer benutzerfreundlichen, lokalisierten Beschreibung ausgedrückt werden, z. b. "Microsoft Outlook 2000 oder höher".
-   Definiert die URLs, die der Protokollhandler standardmäßig verarbeiten soll.

### <a name="isearchprotocoloptions"></a>Isearchprotocoloptions

In der folgenden Tabelle werden die Methoden beschrieben, die Sie für die **isearchprotocoloptions** -Schnittstelle implementieren müssen.



| Methode               | BESCHREIBUNG                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| Prüfanforderungen    | Bestimmt, ob die Mindestanforderungen eines benutzerdefinierten Protokoll Handlers erfüllt werden.                             |
| Getdefaultcrawlscope | Gibt eine Liste von Standard-URLs in einem angegebenen Speicher für einen benutzerdefinierten Protokollhandler zurück.                   |
| Getrequierungen      | Identifiziert eine benutzerfreundliche, lokalisierte Beschreibung der Mindestanforderungen für einen benutzerdefinierten Protokollhandler. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Benachrichtigen des Index von Änderungen](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Hinzufügen von Symbolen, Vorschauen und Kontextmenüs mit Shellerweiterungen](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Installieren und Registrieren von Protokoll Handlern](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 