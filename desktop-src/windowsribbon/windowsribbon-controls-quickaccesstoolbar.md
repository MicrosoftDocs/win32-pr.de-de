---
title: Symbolleiste für den Schnellzugriff
description: Die Symbolleiste für den schnell Zugriff (QAT) ist eine kleine, anpassbare Symbolleiste, die eine Reihe von Befehlen verfügbar macht, die von der Anwendung angegeben oder vom Benutzer ausgewählt werden.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039007"
---
# <a name="quick-access-toolbar"></a>Symbolleiste für den Schnellzugriff

Die Symbolleiste für den schnell Zugriff (QAT) ist eine kleine, anpassbare Symbolleiste, die eine Reihe von Befehlen verfügbar macht, die von der Anwendung angegeben oder vom Benutzer ausgewählt werden.

- [Introduction (Einführung)](#introduction)
- [Implementieren der Symbolleiste für den schnell Zugriff](#implement-the-quick-access-toolbar)
  - [Markup](#markup)
  - [Code](#code)
- [QAT-Persistenz](#qat-persistence)
- [Symbolleisten Eigenschaften für den schnell Zugriff](#quick-access-toolbar-properties)
- [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Standardmäßig befindet sich die Symbolleiste für den schnell Zugriff (QAT) in der Titelleiste des Anwendungsfensters, kann jedoch so konfiguriert werden, dass Sie unter dem Menüband angezeigt wird. Neben der Bereitstellung von Befehlen enthält auch die Symbolleiste für den schnell Zugriff (QAT) ein anpassbares Dropdown Menü, das den vollständigen Satz der Standard Befehle für die schnell Zugriffs Symbolleiste (in der Symbolleiste für den schnell Zugriff) und die Menü Band Optionen enthält.

Der folgende Screenshot zeigt ein Beispiel für die Symbolleiste für den schnell Zugriff auf das Menüband (QAT).

![Screenshot von QAT im Microsoft Paint-Menüband.](images/markup/qat-and-menu.png)

Die Symbolleiste für den schnell Zugriff (QAT) besteht aus einer Kombination aus bis zu 20 Befehlen, die entweder von der Anwendung (als "Anwendungsstandard Liste" bezeichnet) oder vom Benutzer ausgewählt wurden. Die Symbolleiste für den schnell Zugriff (QAT) kann eindeutige Befehle enthalten, die an anderer Stelle der Multifunktionsleisten-Benutzeroberfläche nicht verfügbar sind.

> [!Note]
> Während fast alle multifunktionsleistensteuerelemente zulassen, dass der zugehörige Befehl der Symbolleiste für den schnell Zugriff (QAT) über das im folgenden Screenshot gezeigte Kontextmenü hinzugefügt wird, stellen Befehle, die in einem [Kontext-Popup](windowsribbon-controls-contextpopup.md) verfügbar gemacht werden, dieses Kontextmenü nicht bereit.
>
> ![Screenshot des Befehls Kontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Implementieren der Symbolleiste für den schnell Zugriff

Wie bei allen Windows-Menü Band Framework-Steuerelementen erfordert die vollständige Nutzung der Symbolleiste für den schnell Zugriff (QAT) sowohl eine Markup Komponente, die ihre Darstellung innerhalb des Menübands steuert, als auch eine Code Komponente, die ihre Funktionalität regelt.

### <a name="markup"></a>Markup

Das Steuerelement für die schnell Zugriff-Symbolleiste (QAT) wurde deklariert und mit einer Befehls-ID im Markup über das [quickaccesstoolbar](windowsribbon-element-quickaccesstoolbar.md) -Element verknüpft. Die Befehls-ID wird verwendet, um die Symbolleiste für den schnell Zugriff (QAT) an einen von der Anwendung definierten Befehls Handler zu identifizieren und zu binden.

Zusätzlich zum grundlegenden Befehls Handler für die primäre Funktion für die schnell Zugriff-Symbolleiste (QAT) wird durch das Deklarieren des optionalen *customizecommandname* [quickaccesstoolbar](windowsribbon-element-quickaccesstoolbar.md) -Element Attributs der Befehlsliste im Dropdown Menü für den schnell Zugriff, für den ein sekundärer Befehls Handler definiert werden muss, ein **mehr** Befehls Element hinzugefügt.

Um Konsistenz zwischen Multifunktionsleisten-Anwendungen zu gewährleisten, wird empfohlen, dass der *customizecommandname* -Befehls Handler das Anpassungs Dialogfeld für den schnell Zugriff (QAT) startet. Da das Multifunktionsleisten Framework nur den Ausgangspunkt in der Benutzeroberfläche bereitstellt, ist die Anwendung allein dafür verantwortlich, die Anpassungs dialogdialogfeld-Implementierung bereitzustellen, wenn die Rückruf Benachrichtigung für diesen Befehl empfangen wird.

Der folgende Screenshot zeigt das Dropdown Menü für den schnell Zugriff-Symbolleiste (QAT) mit dem Befehls Element **Weitere Befehle** .

![Screenshot eines QAT-Menüs mit den weiteren Befehlen... Befehls Element.](images/markup/qat-customizecommandname.png)

Die Liste mit den Anwendungs Standardwerten für die Symbolleiste für den schnell Zugriff (QAT) wird über die [quickaccesstoolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) -Eigenschaft angegeben, die eine Standardliste empfohlener Befehle identifiziert, die alle im Dropdown Menü schnell Zugriff-Symbolleiste (QAT) aufgelistet sind.

Zum Anzeigen von Befehlen aus der Liste Anwendungs Standardwerte auf der Symbolleiste für die schnell Zugriffs Symbolleiste (QAT) muss das *ApplicationDefaults. IsChecked* -Attribut jedes Steuer Elements den Wert aufweisen `true` . In den vorangehenden Bildern werden die Ergebnisse der Einstellung dieses Attributs auf `true` für die Befehle zum **Speichern**, Rückgängigmachen und wieder **holen** angezeigt. 

[Quickaccesstoolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) unterstützt drei Typen von Menü Band Steuerelementen: [Schalt](windowsribbon-controls-button.md)Fläche, [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md)und [Kontrollkästchen](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 und höher: alle Katalog basierten Steuerelemente werden unterstützt ([ComboBox](windowsribbon-element-combobox.md), [inribbongallery](windowsribbon-element-inribbongallery.md), [splitbuttongallery](windowsribbon-element-splitbuttongallery.md)und [dropdowngallery](windowsribbon-element-dropdowngallery.md)).
>
> Elemente in einem Katalog-Steuerelement können Hervorhebung bei Hover unterstützen. Zur Unterstützung der Hover-Hervorhebung muss der Katalog ein Element Katalog sein und ein [flowmenulayout](windowsribbon-element-flowmenulayout.md) des Typs [verticalmenulayout](windowsribbon-element-verticalmenulayout.md)verwenden.

Im folgenden Beispiel wird das grundlegende Markup für ein [quickaccesstoolbar](windowsribbon-element-quickaccesstoolbar.md) -Element veranschaulicht.

In diesem Code Abschnitt werden die Befehls Deklarationen für ein Element für die [schnell Zugriffs Symbolleiste (QAT)](windowsribbon-element-quickaccesstoolbar.md) gezeigt.

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

Dieser Code Abschnitt zeigt die Steuerelement Deklarationen für ein Element für die [schnell Zugriffs Symbolleiste (QAT)](windowsribbon-element-quickaccesstoolbar.md) .

```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```

### <a name="code"></a>Code

Die Menüband-Framework-Anwendung muss eine Befehls Handler-Rückruf Methode bereitstellen, um die Symbolleiste für den schnell Zugriff zu bearbeiten. Dieser Handler funktioniert ähnlich wie Befehls Katalog Handler, mit der Ausnahme, dass die Symbolleiste für den schnell Zugriff (QAT) keine Kategorien unterstützt. Weitere Informationen finden Sie unter [Arbeiten mit Galerien](ribbon-controls-galleries.md).

Die Befehls Auflistung für die schnell Zugriff-Symbolleiste (QAT) wird als [iuicollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt über den [UI \_ pkey \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) -Eigenschafts Schlüssel abgerufen. Sie können der Symbolleiste für den schnell Zugriff (QAT) zur Laufzeit Befehle hinzufügen, indem Sie der **iuicollection** ein [iuisimplepropertyset](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt hinzufügen.

Im Unterschied zu Befehls Galerien ist eine Eigenschaft des Befehls Typs ([UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) für das [iuisimplepropertyset](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt der schnell Zugriffs Symbolleiste (QAT) nicht erforderlich. Allerdings muss der Befehl im Menüband oder in der Symbolleiste für die schnell Zugriffs Symbolleiste (QAT) mit der Standardliste der Anwendungen ein neuer Befehl kann nicht zur Laufzeit erstellt und der Symbolleiste für den schnell Zugriff hinzugefügt werden.

> [!Note]  
> Die Menüband-Anwendung kann die [iuicollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) für den schnell Zugriff (QAT) nicht durch ein benutzerdefiniertes Sammlungsobjekt ersetzen, das von IEnumUnknown abgeleitet ist.

Das folgende Beispiel veranschaulicht eine einfache Implementierung des Befehls Handlers für die schnell Zugriffs Symbolleiste (QAT).

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a>QAT-Persistenz

Die Befehls Elemente und-Einstellungen für die schnell Zugriffs Symbolleiste (QAT) können über Anwendungs Sitzungen hinweg beibehalten werden, indem die Funktionen " [iuiribbon:: savesettingstostream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) " und " [iuiribbon:: loadsettingsfromstream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) " verwendet werden. Weitere Informationen finden Sie unter [persistenzstatus der Multifunktionsleiste](ribbon-statepersistence.md).

## <a name="quick-access-toolbar-properties"></a>Symbolleisten Eigenschaften für den schnell Zugriff

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Steuerelement für die schnell Zugriffs Symbolleiste (QAT).

In der Regel wird eine Eigenschaft für die schnell Zugriffs Symbolleiste (QAT) in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Aufrufen der [iuiframework:: invalidateuicommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [iuicommandhandler:: updateproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [iuicommandhandler:: updateproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [iuiframework:: getuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [iuiframework:: setuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die mit dem Steuerelement für die schnell Zugriffs Symbolleiste (QAT) verknüpft sind.

| Eigenschafts Schlüssel | Notizen |
|---|---|
| [UI- \_ pkey \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) | Unterstützt [iuiframework:: getuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (bietet keine Unterstützung für [iuiframework:: mintuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [Iuiframework:: getuicommandproperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) gibt einen Zeiger auf ein iuicollection-Objekt zurück, das die Befehle in der QAT darstellt. Jeder Befehl wird durch die Befehls-ID identifiziert, die durch Aufrufen der [iuisimplepropertyset:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) -Methode abgerufen wird, und übergibt den Eigenschafts Schlüssel [UI \_ pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md). |

Dem Befehls Element " **Weitere Befehle** " im Dropdown Menü "schnell Zugriff" (QAT) sind keine Eigenschafts Schlüssel zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

- [Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
- [Quickaccesstoolbar-Markup Element](windowsribbon-element-quickaccesstoolbar.md)