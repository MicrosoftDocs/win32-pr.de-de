---
title: Symbolleiste für den Schnellzugriff
description: Die Quick Access Toolbar (QAT) ist eine kleine, anpassbare Symbolleiste, die eine Reihe von Befehlen verfügbar macht, die von der Anwendung angegeben oder vom Benutzer ausgewählt werden.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d63eb3f7b1a2c1213430f86a9a12fe4517c738290ed736eb1d356420aa145cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110725"
---
# <a name="quick-access-toolbar"></a>Symbolleiste für den Schnellzugriff

Die Quick Access Toolbar (QAT) ist eine kleine, anpassbare Symbolleiste, die eine Reihe von Befehlen verfügbar macht, die von der Anwendung angegeben oder vom Benutzer ausgewählt werden.

- [Introduction (Einführung)](#introduction)
- [Implementieren der Symbolleiste für den Schnellzugriff](#implement-the-quick-access-toolbar)
  - [Markup](#markup)
  - [Code](#code)
- [QAT-Persistenz](#qat-persistence)
- [Eigenschaften der Schnellzugriffssymbolleiste](#quick-access-toolbar-properties)
- [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Standardmäßig befindet sich die Symbolleiste für den Schnellzugriff (Quick Access Toolbar, QAT) in der Titelleiste des Anwendungsfensters, kann aber so konfiguriert werden, dass sie unterhalb des Menübands angezeigt wird. Zusätzlich zum Verfügbar machen von Befehlen enthält die Symbolleiste für den Schnellzugriff (QAT) auch ein anpassbares Dropdownmenü, das den vollständigen Satz von QAT-Standardbefehlen (Quick Access Toolbar) enthält (ob ausgeblendet oder in der Symbolleiste für den Schnellzugriff (QAT)) angezeigt) sowie eine Reihe von Symbolleisten für den Schnellzugriff (Quick Access Toolbar, QAT) und Menübandoptionen.

Der folgende Screenshot zeigt ein Beispiel für die Symbolleiste für den Menüband-Schnellzugriff (QAT).

![Screenshot der Qat im Microsoft Paint-Menüband.](images/markup/qat-and-menu.png)

Die Symbolleiste für den Schnellzugriff (QAT) besteht aus einer Kombination von bis zu 20 Befehlen, die entweder von der Anwendung angegeben (als Standardliste der Anwendung bezeichnet) oder vom Benutzer ausgewählt werden. Die Symbolleiste für den Schnellzugriff (Quick Access Toolbar, QAT) kann eindeutige Befehle enthalten, die an anderer Stelle auf der Menübandbenutzeroberfläche nicht verfügbar sind.

> [!Note]
> Während fast alle Menübandsteuerelemente zulassen, dass ihr zugeordneter Befehl der Symbolleiste für den Schnellzugriff (QAT) über das kontextmenü hinzugefügt wird, das im folgenden Screenshot gezeigt wird, stellen Befehle, die in einem [Kontext-Popup](windowsribbon-controls-contextpopup.md) verfügbar gemacht werden, dieses Kontextmenü nicht zur Verfügung.
>
> ![Screenshot des Befehlskontextmenüs im Microsoft Paint-Menüband.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Implementieren der Symbolleiste für den Schnellzugriff

Wie bei allen Windows-Frameworksteuerelementen des Menübands erfordert die vollständige Nutzung der Quick Access Toolbar (QAT) sowohl eine Markupkomponente, die die Darstellung im Menüband steuert, als auch eine Codekomponente, die deren Funktionalität steuert.

### <a name="markup"></a>Markup

Das QAT-Steuerelement (Quick Access Toolbar) wird im Markup über das [QuickAccessToolbar-Element](windowsribbon-element-quickaccesstoolbar.md) deklariert und einer Befehls-ID zugeordnet. Die Befehls-ID wird verwendet, um die Quick Access Toolbar (QAT) zu identifizieren und an einen befehlshandler zu binden, der von der Anwendung definiert wird.

Zusätzlich zum grundlegenden Befehlshandler für die primäre QAT-Funktionalität (Quick Access Toolbar) bewirkt das Deklarieren des  optionalen *CustomizeCommandName* [QuickAccessToolbar-Elementattributs,](windowsribbon-element-quickaccesstoolbar.md) dass das Framework der Befehlsliste des Dropdownmenüs der Symbolleiste für den Schnellzugriff (QAT) ein Element weitere Befehle hinzufüge, für das ein sekundärer Befehlshandler definiert werden muss.

Für konsistenzübergreifende Menübandanwendungen wird empfohlen, dass der *Befehlshandler CustomizeCommandName* ein Dialogfeld zur Anpassung der Symbolleiste für den Schnellzugriff (Quick Access Toolbar, QAT) startet. Da das Menübandframework nur den Startpunkt in der Benutzeroberfläche bietet, ist die Anwendung allein für die Bereitstellung der Implementierung des Anpassungsdialogfelds verantwortlich, wenn die Rückrufbenachrichtigung für diesen Befehl empfangen wird.

Der folgende Screenshot zeigt das Dropdownmenü Quick Access Toolbar (QAT) mit dem **Befehlselement Weitere** Befehle.

![Screenshot eines Qat-Menüs mit den mehr Befehlen... Befehlselement.](images/markup/qat-customizecommandname.png)

Die Standardliste der Anwendung für die Quick Access Toolbar (QAT) wird über die [QuickAccessToolbar.ApplicationDefaults-Eigenschaft](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) angegeben, die eine Standardliste empfohlener Befehle identifiziert, die alle im Dropdownmenü Quick Access Toolbar (QAT) aufgeführt sind.

Zum Anzeigen von Befehlen aus der Liste der Standardeinstellungen der Anwendung auf der Symbolleiste der Symbolleiste für den Schnellzugriff (QAT) muss das *ApplicationDefaults.IsChecked-Attribut* jedes Steuerelementelements den Wert `true` haben. Die obigen Abbildungen zeigen die Ergebnisse der Festlegung dieses Attributs auf für die `true` **Befehle "Speichern",** **"Rückgängig"** und **"Wiederholen".**

[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) unterstützt drei Arten [](windowsribbon-controls-button.md)von Menüband-Steuerelementen: Schaltfläche , [Umschaltfläche](windowsribbon-controls-togglebutton.md)und [Kontrollkästchen](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 und neuer: Alle katalogbasierten Steuerelemente werden unterstützt ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)und [DropDownGallery](windowsribbon-element-dropdowngallery.md)).
>
> Elemente in einem Katalogsteuerelementen können die Hervorhebung beim Hovern unterstützen. Um Hoverhervorhebungen zu unterstützen, muss der Katalog ein Objektkatalog sein und [ein FlowMenuLayout](windowsribbon-element-flowmenulayout.md) vom Typ [VerticalMenuLayout verwenden.](windowsribbon-element-verticalmenulayout.md)

Im folgenden Beispiel wird das grundlegende Markup für ein [QuickAccessToolbar-Element](windowsribbon-element-quickaccesstoolbar.md) veranschaulicht.

Dieser Codeabschnitt zeigt die Befehlsdeklarationen für ein [QAT-Element (Quick Access Toolbar).](windowsribbon-element-quickaccesstoolbar.md)

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

Dieser Codeabschnitt zeigt die Steuerelementdeklarationen für ein [QAT-Element (Quick Access Toolbar).](windowsribbon-element-quickaccesstoolbar.md)

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

Die Menüband-Frameworkanwendung muss eine Befehlshandler-Rückrufmethode bereitstellen, um die Quick Access Toolbar (QAT) zu bearbeiten. Dieser Handler funktioniert ähnlich wie Befehlskataloghandler, mit der Ausnahme, dass die Symbolleiste für den Schnellzugriff (QAT) keine Kategorien unterstützt. Weitere Informationen finden Sie unter [Arbeiten mit Katalogen.](ribbon-controls-galleries.md)

Die Sammlung von QAT-Befehlen (Quick Access Toolbar) wird als [IUICollection-Objekt](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) über den [ \_ PKEY \_ ItemsSource-Eigenschaftsschlüssel](windowsribbon-reference-properties-uipkey-itemssource.md) der Benutzeroberfläche abgerufen. Das Hinzufügen von Befehlen zur Quick Access Toolbar (QAT) zur Laufzeit erfolgt durch Hinzufügen eines [IUISimplePropertySet-Objekts](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) zur **IUICollection**.

Im Gegensatz zu Befehlsgalerien ist für das [IUISimplePropertySet-Objekt](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) der Quick Access Toolbar (QAT) keine Befehlstypeigenschaft ([ \_ UI PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) erforderlich. Der Befehl muss jedoch im Menüband oder in der Standardliste der QAT-Anwendung (Quick Access Toolbar) vorhanden sein. Ein neuer Befehl kann zur Laufzeit nicht erstellt und der Symbolleiste für den Schnellzugriff (QAT) hinzugefügt werden.

> [!Note]  
> Die Menübandanwendung kann die [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) der Symbolleiste für den Schnellzugriff (Quick Access Toolbar, QAT) nicht durch ein benutzerdefiniertes Sammlungsobjekt ersetzen, das von IEnumUnknown abgeleitet wurde.

Im folgenden Beispiel wird eine grundlegende Implementierung des QAT-Befehlshandlers (Quick Access Toolbar) veranschaulicht.

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

Befehle und Einstellungen der Symbolleiste für den Schnellzugriff (Quick Access Toolbar, QAT) können mithilfe der [Funktionen IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) und [IUIRibbon::LoadSettingsFromStream sitzungsübergreifend](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) beibehalten werden. Weitere Informationen finden Sie unter [Beibehalten des Menübandzustands.](ribbon-statepersistence.md)

## <a name="quick-access-toolbar-properties"></a>Eigenschaften der Schnellzugriffssymbolleiste

Das Menübandframework definiert eine Sammlung von [Eigenschaftsschlüsseln für](windowsribbon-reference-properties.md) das QAT-Steuerelement (Quick Access Toolbar).

In der Regel wird eine QAT-Eigenschaft (Quick Access Toolbar) in der Menübandbenutzeroberfläche aktualisiert, indem der befehl, der dem Steuerelement zugeordnet ist, durch einen Aufruf der [IUIFramework::InvalidateUICommand-Methode](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [IUICommandHandler::UpdateProperty-Rückrufmethode](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [IUICommandHandler::UpdateProperty-Rückrufmethode](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menübandbenutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [IUIFramework::GetUICommandProperty-Methode](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [IUIFramework::SetUICommandProperty-Methode](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem QAT-Steuerelement (Quick Access Toolbar) zugeordnet sind.

| Eigenschaftsschlüssel | Hinweise |
|---|---|
| [\_PKEY-Elemente der \_ BenutzeroberflächeQuelle](windowsribbon-reference-properties-uipkey-itemssource.md) | Unterstützt [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (unterstützt [IUIFramework::SetUICommandProperty nicht).](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) gibt einen Zeiger auf ein IUICollection-Objekt zurück, das die Befehle in der QAT darstellt. Jeder Befehl wird durch seine Befehls-ID identifiziert, die durch Aufrufen der [IUISimplePropertySet::GetValue-Methode](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) und Übergeben der Eigenschaftenschlüssel-UI [ \_ PKEY \_ CommandId ermittelt wird.](windowsribbon-reference-properties-uipkey-commandid.md) |

Dem Befehlselement Weitere  Befehle im Dropdownmenü der Symbolleiste für den Schnellzugriff (QAT) sind keine Eigenschaftsschlüssel zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

- [Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
- [QuickAccessToolbar-Markupelement](windowsribbon-element-quickaccesstoolbar.md)