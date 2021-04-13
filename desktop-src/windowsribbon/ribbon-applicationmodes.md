---
title: Neukonfigurieren des Menübands mit Anwendungsmodi
description: Das Windows-Menüband-Framework unterstützt die dynamische Neukonfiguration und das verfügbar machen von Kernelementen der Menüband-Benutzeroberfläche zur Laufzeit basierend auf dem Zustand der Anwendung (auch als Kontext bezeichnet).
ms.assetid: 8e9d85c5-33e4-4212-b9e4-2fc3b492c273
keywords:
- Windows-Menüband, Neukonfiguration mit Anwendungsmodi
- Multifunktionsleiste, Neukonfiguration mit Anwendungsmodi
- Neukonfigurieren von Windows-Menüband mit Anwendungsmodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d206c238e6fe7463562077daaa52a5522a79d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390334"
---
# <a name="reconfiguring-the-ribbon-with-application-modes"></a>Neukonfigurieren des Menübands mit Anwendungsmodi

Das Windows-Menüband-Framework unterstützt die dynamische Neukonfiguration und das verfügbar machen von Kernelementen der Menüband-Benutzeroberfläche zur Laufzeit basierend auf dem Zustand der Anwendung (auch als Kontext bezeichnet). Die verschiedenen Zustände, die von einer Anwendung unterstützt werden, werden als Anwendungsmodi bezeichnet und mit bestimmten Elementen im Markup verknüpft.

-   [Introduction (Einführung)](#introduction)
-   [Kontextabhängige Benutzeroberfläche](#contextual-user-interface)
    -   [Ein Szenario mit einfachem Anwendungsmodus](#a-simple-application-mode-scenario)
-   [Implementieren von Anwendungsmodi](#implementing-application-modes)
    -   [Identifizieren der Modi](#identify-the-modes)
    -   [Zuweisen von Steuerelementen zu Anwendungsmodi](#assign-controls-to-application-modes)
    -   [Wechseln von Modi zur Laufzeit](#switch-modes-at-runtime)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Anwendungsmodi bestehen aus logischen Gruppen von Steuerelementen, die in der Menüband-Benutzeroberfläche einige Kern Anwendungsfunktionen verfügbar machen. Diese Modi werden von der Anwendung dynamisch aktiviert oder deaktiviert, indem die Framework-Methode [**iuiframework:: setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)aufgerufen wird, die die Sichtbarkeit von mindestens einem Anwendungsmodus aktiviert oder deaktiviert.

## <a name="contextual-user-interface"></a>Kontextabhängige Benutzeroberfläche

Das Menüband-Framework bietet umfassende Benutzer Funktionen, indem dynamische Steuerelemente integriert werden, die nahtlos auf die Benutzerinteraktion und den Anwendungskontext reagieren. Diese umfangreiche kontextbezogene Benutzeroberfläche wird durch eine Kombination der folgenden Mechanismen bereitgestellt:

-   Kataloge: Sammlungs basierte Steuerelemente, die die dynamische Bearbeitung Ihrer Element Auflistungen unterstützen.
-   Kontextabhängige Registerkarten: Menüband-Registerkarten, deren Sichtbarkeit durch eine Änderung im Arbeitsbereichs Kontext bestimmt wird, z. b. die Auswahl eines Bilds in einem Dokument.
-   Anwendungsmodi: Kern Anwendungsfunktionen, die vom Anwendungskontext abhängig sind.

In gewisser Hinsicht ähneln Anwendungsmodi funktionell den Kontext Registerkarten. Der grundlegende Unterschied liegt jedoch in der Absicht und dem Bereich jeder.

Kontextbezogene Steuerelemente werden als Reaktion auf eine Änderung des Kontexts in einer Anwendung aktiviert. Beispielsweise wird in Microsoft Paint für Windows 7 eine kontextbezogene Registerkarte angezeigt, die Gruppen von Text bezogenen Befehlen enthält, wenn ein Benutzer einen Textbereich in den Arbeitsbereich einfügt. Diese Kontext Registerkarte enthält keine Kern Befehle für die Anwendung und wird nur in der Benutzeroberfläche verfügbar gemacht, da sich der Kontext *innerhalb* der Anwendung geändert hat. Die Kernfunktionalität der Anwendung (die Befehle zum Bearbeiten von Bildern) ist nach wie vor relevant und für den Benutzer verfügbar, auch wenn die Kontext Registerkarte sichtbar ist.

Anwendungsmodi unterscheiden sich von kontextbezogenen Steuerelementen darin, dass Sie die Funktionalität als Reaktion auf Änderungen im Kontext, in dem die Anwendung ausgeführt wird, neu konfigurieren. Anwendungsmodi befinden sich auf einer höheren Abstraktions Ebene. Sie bieten eine Möglichkeit, die Kernfunktionen einer Anwendung neu zu konfigurieren, anstatt vorübergehend Funktionen verfügbar zu machen, bei denen es sich nicht um eine Kernkomponente der Benutzeroberfläche handelt. Beispielsweise tritt in Microsoft Paint für Windows 7 ein Switch im Anwendungsmodus auf, wenn der Befehl " **Druckvorschau** " aufgerufen wird. Wenn Microsoft Paint zur **Druckvorschau** wechselt, ändert sich der Kontext, in dem die Anwendung ausgeführt wird, von der Bearbeitung in die Vorschau. Folglich wird die Kernfunktionalität der Anwendung geändert, bis die Seiten **Ansicht** abgebrochen wird und die Anwendung erneut in den Bearbeitungs Kontext wechselt.

### <a name="a-simple-application-mode-scenario"></a>Ein Szenario mit einfachem Anwendungsmodus

Im folgenden Szenario wird veranschaulicht, wie Anwendungsmodi in einer Anwendung namens ribbonapp verwendet werden, um diskrete Aspekte der Kernfunktionalität verfügbar zu machen.

In ribbonapp sind zwei Anwendungsmodi definiert:

-   Der einfache Modus macht in der Menüband-Benutzeroberfläche **einfache** Befehle verfügbar. Diese Befehle werden immer angezeigt, unabhängig davon, welcher Anwendungsmodus aktiv ist.
-   Der **Erweiterte** Modus macht komplexe Befehle verfügbar, die für Benutzer von Experten der Anwendung vorgesehen sind. Diese erweiterten Befehle werden neben den einfachen Befehlen in der Multifunktionsleisten-Benutzeroberfläche angezeigt.

Standardmäßig wird ribbonapp im **einfachen** Modus geöffnet, und die für Anfänger benötigten Befehle werden im **Anwendungsmenü** und auf der Registerkarte **Home** angezeigt. Die folgenden Screenshots zeigen das ribbonapp- **Anwendungsmenü** und die Registerkarte " **Home** " im **einfachen** Modus, wobei die modalen Steuerelemente hervorgehoben werden.

![Screenshot, der eine Registerkarte für den einfachen Anwendungsmodus anzeigt](images/overviews/appmode-hometab.png)![Screenshot, der das Anwendungsmenü für den einfachen Anwendungsmodus anzeigt](images/overviews/appmode-simpleappmenu.png)

Obwohl diese Befehle für Einsteiger ausreichend sein können, unterstützt die ribbonapp auch expertenbenutzer über einen **erweiterten** Modus, der bei Aktivierung durch Klicken auf die Schaltfläche **zum erweiterten Modus wechseln** im **Anwendungsmenü** zusätzliche Kernfunktionen anzeigt.

Dieses Szenario kann problemlos implementiert werden, indem verschiedene Elemente im Markup an diskrete Anwendungsmodi gebunden werden, die nach Bedarf aktiviert oder deaktiviert werden können. Die folgenden Screenshots zeigen das ribbonapp- **Anwendungsmenü** und die Registerkarte " **Home** " im **erweiterten** Modus, wobei die modalen Steuerelemente hervorgehoben werden.

![Screenshot, der eine Registerkarte für den erweiterten Anwendungsmodus anzeigt.](images/overviews/appmode-advancedtab.png)![Screenshot, der das Anwendungsmenü für den erweiterten Anwendungsmodus anzeigt](images/overviews/appmode-advancedappmenu.png)

## <a name="implementing-application-modes"></a>Implementieren von Anwendungsmodi

In diesem Abschnitt werden die drei Schritte beschrieben, die in der Regel für die Implementierung von Menüband-Framework-Anwendungsmodi Ribbonapp wird verwendet, um ein Beispiel für jeden Schritt bereitzustellen.

### <a name="identify-the-modes"></a>Identifizieren der Modi

Jeder Modus in einer Anwendung sollte einen logischen Funktions Satz darstellen, der von dem Kontext abhängig ist, in dem eine Anwendung arbeiten kann. Wenn eine Anwendung z. b. Steuerelemente anzeigt, die nur relevant sind, wenn eine Netzwerkverbindung erkannt wird, arbeiten diese Steuerelemente innerhalb eines Netzwerk Kontexts, der die Erstellung eines **Netzwerk** Modus rechtfertigen könnte.

Ribbonapp verfügt über zwei Kontexte, die zu einem beliebigen Zeitpunkt aktiv sein können: **einfach** und **erweitert**. Daher erfordert ribbonapp zwei Modi: **einfach** und **erweitert**.

### <a name="assign-controls-to-application-modes"></a>Zuweisen von Steuerelementen zu Anwendungsmodi

Nachdem die Anwendungsmodi identifiziert wurden, weisen Sie jedes Menüband-Steuerelement einem Modus zu, indem Sie für Steuerelemente, die Anwendungsmodi unterstützen, ein *applicationmodes* -Attribut im Markup deklarieren.

Die Menü Band Ansicht ermöglicht das Angeben von Modi für die folgenden Steuerelemente:

-   Kern [**Register**](windowsribbon-element-tab.md) Kartenelemente.
-   [**Gruppieren**](windowsribbon-element-group.md) Sie Elemente, die untergeordnete Elemente eines Kern [**Register**](windowsribbon-element-tab.md) Karten Elements sind.
-   [**Schalt**](windowsribbon-element-button.md)Flächen-, [**SplitButton**](windowsribbon-element-splitbutton.md)-und [**DropDownButton**](windowsribbon-element-dropdownbutton.md) -Elemente, die einer [**MenuGroup**](windowsribbon-element-menugroup.md) im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)zugewiesen sind.
    > [!Note]  
    > [**Schalt**](windowsribbon-element-button.md)Flächen-, [**SplitButton**](windowsribbon-element-splitbutton.md)-und [**DropDownButton**](windowsribbon-element-dropdownbutton.md) -Elemente können nur dann einem Modus zugewiesen werden, wenn Sie im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)gehostet werden.

     

Im Menüband-Framework werden diese Steuerelemente als modale Steuerelemente bezeichnet. Sie werden nur angezeigt, wenn ein Modus, an den Sie gebunden sind, in der Benutzeroberfläche aktiv ist.

Steuerelemente, die in einem modalen Steuerelement enthalten sind, erben das Verhalten des Anwendungsmodus. Wenn z. b. ein modales [**Gruppen**](windowsribbon-element-group.md) Steuerelement einem **erweiterten** Modus zugewiesen ist und der **Erweiterte** Modus nicht aktiv ist, werden diese **Gruppe** und alle darin vorgesehenen Steuerelemente, modal oder anderweitig, auf der Multifunktionsleisten-Benutzeroberfläche nicht angezeigt.

Mit der Verwendung des *applicationmodes* -Attributs werden Modi modalen Steuerelementen in einer 1: N-Beziehung (1: N) zugewiesen, bei der ein einzelnes modales Steuerelement mit mehreren Modi verknüpft werden kann.

Das Menüband-Framework bezieht sich auf die Zahlen von 0 bis 31 (von 0 bis 31), wobei Modus 0 der Standardmodus ist, der beim Starten einer Menü Bandanwendung automatisch aktiviert wird. Alle modalen Steuerelemente, die kein *applicationmodes* -Attribut angeben, werden als Member des Standardmodus angesehen.

In ribbonapp ist **Simple** der Standardmodus, und die Funktionalität im **erweiterten** Modus wird nur angezeigt, wenn er vom Benutzer initiiert wird.

Im folgenden Beispiel wird das für ribbonapp erforderliche Markup veranschaulicht.


```C++
<Application.Views>
  <Ribbon>

    <!--Application Menu-->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName='cmdAppMenu'>                    
        <MenuGroup>
          <Button CommandName='cmdSave'/>                        
          <Button CommandName='cmdExportMetadata' ApplicationModes='1'/>                   
        </MenuGroup>              
        <MenuGroup>
          <Button CommandName='cmdSwitchModes' ApplicationModes ='0,1'/>
          <Button CommandName='cmdExit'/>
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
            
    <!--Tabs-->
    <Ribbon.Tabs>
      <!--Home Tab-->
      <Tab CommandName='cmdHomeTab'>
                    
        <!--Scaling Policy for Home tab-->
        <Tab.ScalingPolicy>
          <ScalingPolicy>
            <ScalingPolicy.IdealSizes>
              <Scale Group='cmdSimpleControlsGroup' Size='Medium'/>                                
            </ScalingPolicy.IdealSizes>                     
          </ScalingPolicy>
        </Tab.ScalingPolicy>     
                    
        <!--Simple Controls Group-->
        <Group CommandName='cmdSimpleControlsGroup' SizeDefinition='ThreeButtons-OneBigAndTwoSmall'>                        
          <Button CommandName="cmdPaste" />
          <Button CommandName='cmdCut'/>                        
          <Button CommandName='cmdCopy'/>                        
        </Group>
      </Tab>
                
      <!--Advanced Tab-->
      <Tab CommandName='cmdAdvancedTab' ApplicationModes='1'>
        <!--Advanced Controls Group-->
        <Group CommandName='cmdMetadataGroup' ApplicationModes='1' SizeDefinition='TwoButtons'>
          <Button CommandName='cmdEditMetadata' />
          <Button CommandName='cmdCheckErrors' />
        </Group>
      </Tab>
    </Ribbon.Tabs>                   
                             
  </Ribbon>         
</Application.Views>
```



In diesem Beispiel wird Folgendes veranschaulicht:

-   Der Standardmodus 0 muss nicht explizit deklariert werden. Da modale Steuerelemente, die das *applicationmodes* -Attribut nicht angeben, automatisch an den Modus 0 gebunden werden (**einfacher** Modus im ribbonapp-Beispiel), ist es nicht erforderlich, das-Attribut explizit für modale Standard Steuerelemente zu deklarieren.
-   Steuerelemente können an mehrere Modi gebunden werden. Bei ribbonapp ist die Schaltfläche die einzige Anforderung für das *applicationmodes* -Attribut in einem Steuerelement im **einfachen** Modus `cmdSwitchModes` , da es Teil des **einfachen** und **erweiterten** Modus ist. Wenn einer der beiden Modi aktiv ist, wird dieses Steuerelement im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)angezeigt.
-   Modale Steuerelemente erben nicht von ihren übergeordneten Elementen. Die Registerkarte " **erweitert** " von ribbonapp enthält eine **metadatengruppe** . Beide modalen Steuerelemente werden **dem Modus 1 (** erweiterter Modus) zugewiesen. Durch das Zuweisen der Registerkarte " **erweitert** " zu Modus 1 werden untergeordnete Steuerelemente wie die **metadatengruppe** nicht automatisch zu Modus 1 zugewiesen. Dadurch kann jede Gruppe innerhalb einer Registerkarte zur Laufzeit unabhängig aktiviert oder deaktiviert werden.
-   Nicht modale Steuerelemente können weiterhin auf modusswitches zurückgreifen. Die Schaltflächen **Edit Metadata** und **Check for Errors** von ribbonapp sind für fortgeschrittene Benutzer und nur verfügbar, wenn der Benutzer in den **erweiterten** Modus wechselt. Schaltflächen-Steuerelemente, die nicht im [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) gehostet werden, sind nicht modal. Da diese Schaltflächen jedoch in einem modalen Steuerelement (der **metadatengruppe** ) gehostet werden, sind Sie sichtbar, wenn die Gruppe sichtbar ist. Diese Schaltflächen werden daher angezeigt, wenn der erweiterte Modus aktiviert und die **metadatengruppe** in der Menüband-Benutzeroberfläche verfügbar gemacht wird.

### <a name="switch-modes-at-runtime"></a>Wechseln von Modi zur Laufzeit

Nachdem Modi im Markup definiert wurden, können Sie als Reaktion auf Kontext Ereignisse problemlos aktiviert oder deaktiviert werden. Wie bereits erwähnt, werden Menüband-Anwendungen immer im Standardmodus 0 gestartet. Nachdem die Anwendung initialisiert wurde und Modus 0 aktiv ist, kann der Satz aktiver Modi durch Aufrufen der [**iuiframework:: setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) -Funktion geändert werden. Diese Funktion nimmt eine 32-Bit-Ganzzahl als bitweise Darstellung der Modi an, die aktiv sein sollen. das unwichtigste Bit steht für Modus 0 und das signifikanteste Bit steht für Modus 31. Wenn ein Bit auf 0 (null) festgelegt ist, ist der Modus auf der Menüband-Benutzeroberfläche nicht aktiv.

Wenn ein Benutzer in ribbonapp den **erweiterten** Modus aktiviert, werden die erweiterten Befehle neben den einfachen Befehlen angezeigt. Der Befehls Handler für die Schaltfläche zu erweiterter **Modus wechseln** ruft [**iuiframework:: setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) auf, um die Modi 0 (**einfach**) und 1 (**erweitert**) auf der Benutzeroberfläche als aktiv festzulegen. Das folgende Beispiel zeigt den ribbonapp-Code für diesen Funktions aufrub:


```C++
const int SIMPLE_MODE = 0;
const int ADVANCED_MODE = 1;
pFramework->SetModes( UI_MAKEAPPMODE(SIMPLE_MODE) | UI_MAKEAPPMODE(ADVANCED_MODE) );
```



> [!Note]  
> Das "Multifunktionsleisten-Framework"- \_ makeappmode-Makro vereinfacht das Festlegen dieser Bits ordnungsgemäß für die Vorbereitung des Aufrufens von [**iuiframework:: setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes).

 

In diesem Beispiel wird Folgendes veranschaulicht:

-   Verwenden Sie das \_ makeappmode-Makro der UI, um einen modussatz zu erstellen.
-   Modi werden explizit und atomarisch festgelegt. Der ganzzahlige Wert, der an [**iuiframework:: setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) übermittelt wird, stellt die Modi dar, die aktiv werden, nachdem die Funktion zurückgegeben wurde. Obwohl der **einfache** Modus zuvor aktiv war, **muss iuiframework:: setmodes** angeben, dass der **einfache** Modus aktiv bleibt, wenn der **Erweiterte** Modus aktiviert wird.
-   Der Standardmodus kann entfernt werden. Obwohl in ribbonapp der Standardmodus (Modus 0) nie entfernt wird, kann er mit dem folgenden-Befehl entfernt werden: `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))` , wobei nur die erweiterten Befehle in der Benutzeroberfläche verfügbar gemacht werden.

> [!Note]  
> Wenn die Modi einer Anwendung neu konfiguriert werden, versucht das Menüband, die zuvor ausgewählte Registerkarte in der Benutzeroberfläche beizubehalten. Wenn der neue Satz von Modi nicht mehr die Registerkarte enthält, die vor dem-Befehl ausgewählt wurde, wählt das Menüband die Registerkarte im Layout aus, die dem [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)am nächsten liegt. Diese Registerkarte soll die Befehle enthalten, die für den Benutzer am relevantesten sind. Weitere Informationen finden Sie unter [Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx)für die Multifunktionsleisten-Benutzer Leistung.

 

## <a name="remarks"></a>Bemerkungen

Das Menüband muss immer über mindestens einen aktiven Modus verfügen. Wenn eine Anwendung versucht, alle Modi durch Aufrufen von [**iuiframework:: setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) mit einem Moduswert von 0 zu deaktivieren, \_ wird E FAIL zurückgegeben, und der aktive modussatz bleibt unverändert.

Das Framework erfordert, dass in der Menüband-Benutzeroberfläche immer mindestens eine Registerkarte vorhanden ist. Folglich muss mindestens eine Registerkarte vom Standardmodus (Modus 0) und nach jedem Modusschalter verfügbar gemacht werden.

Nicht alle Bereiche der Multifunktionsleisten-Benutzeroberfläche sind von Anwendungsmodi betroffen. Wenn beispielsweise die Deaktivierung eines Modus das Verschwinden von Schaltflächen aus dem Menüband bewirkt, die zuvor der [Symbolleiste für den schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md)hinzugefügt wurden, verbleiben diese Schaltflächen auf der Symbolleiste für den schnell Zugriff, sodass Benutzer die an die Schaltflächen gebundenen Befehle ausführen können. Als allgemeine Regel gilt: Wenn ein Befehl zu einem oder mehreren inaktiven Modi gehört, sollte dieser Befehl auch deaktiviert werden, indem die Eigenschaft [UI \_ pkey \_ aktiviert](windowsribbon-reference-properties-uipkey-enabled.md) auf 0 (Variant \_ false) festgelegt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multifunktionsleisten-Benutzeroberflächen Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Anzeigen kontextbezogener Registerkarten](ribbon-contextualtabs.md)
</dt> </dl>

 

 