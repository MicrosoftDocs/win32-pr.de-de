---
title: Implementieren eines Client-Side (Proxy) Benutzeroberflächenautomatisierung Anbieters
description: In diesem Thema wird beschrieben, wie Sie einen Proxyanbieter für ein nicht unterstütztes Steuerelement schreiben und der Liste der Proxys hinzufügen, die von Clientanwendungen verwendet werden.
ms.assetid: c66f4a7b-0a12-4c65-a3e9-1c826d54ac6b
keywords:
- Benutzeroberflächenautomatisierung,clientseitige Anbieterimplementierung
- Benutzeroberflächenautomatisierung,Anbieterimplementierung
- Benutzeroberflächenautomatisierung,implementieren von clientseitigen Anbietern
- Benutzeroberflächenautomatisierung,implementierende Anbieter
- Benutzeroberflächenautomatisierung,Proxys
- proxies
- clientseitige Anbieter
- providers,implementing
- Implementieren clientseitiger Anbieter
- Implementieren von Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8724f0761b5d7e5d361742734901990136a7a98c1b2f541b4fadb69c31a92d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861300"
---
# <a name="implementing-a-client-side-proxy-ui-automation-provider"></a>Implementieren eines Client-Side (Proxy) Benutzeroberflächenautomatisierung Anbieters

Microsoft Benutzeroberflächenautomatisierung stellt eine Reihe von Proxys für die meisten Standardsteuerelemente zur Verfügung, z. B. diejenigen, die in Microsoft Win32, Windows Forms und Windows Presentation Foundation (WPF)-Anwendungen verwendet werden. Viele benutzerdefinierte Steuerelemente und Steuerelemente von Drittanbietern implementieren jedoch keine nativen Benutzeroberflächenautomatisierung Anbieter. Um für Benutzeroberflächenautomatisierung Clientanwendungen zugänglich zu sein, müssen diese Steuerelemente mit clientseitigen Anbietern , auch als Proxyanbieter oder Proxys bezeichnet, *ausgestattet sein.* 

In diesem Thema wird beschrieben, wie Sie einen Proxyanbieter für ein nicht unterstütztes Steuerelement schreiben und der Liste der Proxys hinzufügen, die von Clientanwendungen verwendet werden. Es umfasst die folgenden Themen:

-   [Was ist ein Proxy?](#what-is-a-proxy)
-   [Was ist eine Proxy Factory?](#what-is-a-proxy-factory)
-   [Proxy Factory-Zuordnung](#proxy-factory-mapping)
-   [Verwalten von Standardproxies](#managing-default-proxies)
-   [Zugehörige Themen](#related-topics)

Codebeispiele, die zeigen, wie Proxyanbieter implementiert werden, finden Sie unter Themen zur Benutzeroberflächenautomatisierung [Anbieter.](uiauto-howto-topics-for-uiautomation-providers.md)

## <a name="what-is-a-proxy"></a>Was ist ein Proxy?

Ein clientseitiger Anbieter oder Proxy ist ein Objekt, das die [**IRawElementProviderSimple-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) im Namen eines Steuerelements implementiert, das nicht über eine eigene **IRawElementProviderSimple-Implementierung** verfügt. Ohne Proxy ist ein solches Steuerelement größtenteils undurchsichtig für Benutzeroberflächenautomatisierung, das nur grundlegende Informationen liefern kann, die über das Fensterhand handle **(HWND)** verfügbar sind, z. B. die Position des Steuerelements.

## <a name="what-is-a-proxy-factory"></a>Was ist eine Proxy Factory?

Jeder Proxy erfordert eine entsprechende *Proxyfactory,* bei der es sich um ein Objekt handelt, das die [**IUIAutomationProxyFactory-Schnittstelle verfügbar**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) macht. Benutzeroberflächenautomatisierung verwaltet eine interne Tabelle mit Proxy factory-Einträgen, die jeweils einen Verweis auf die Proxy factory für jeden Proxy und eine Reihe von Bedingungen enthalten. Wenn Benutzeroberflächenautomatisierung auf ein Steuerelement trifft, das nicht über eine native [**IRawElementProviderSimple-Implementierung**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) verfügt, sucht es nach einem Proxy factory-Eintrag, dessen Bedingungen darauf hinweisen, dass es das Steuerelement unterstützt. Benutzeroberflächenautomatisierung Die Tabelle wird von Anfang an durchsucht, und wenn sie einen übereinstimmenden Eintrag findet, ruft Benutzeroberflächenautomatisierung die [**IUIAutomationProxyFactory::CreateProvider-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) der Factory auf. Wenn der übereinstimmende Proxy erfolgreich erstellt wurde, beendet Benutzeroberflächenautomatisierung die Suche und verwendet das neu erstellte Proxyobjekt. Andernfalls Benutzeroberflächenautomatisierung die Suche fort.

Eine Clientanwendung erstellt eine Instanz eines Proxyfactoryeintrags mithilfe der [**IUIAutomation::CreateProxyFactoryEntry-Methode,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) die einen [**IUIAutomationProxyFactoryEntry-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) zurückgibt. Clients verwenden methoden, die **von IUIAutomationProxyFactoryEntry verfügbar** gemacht werden, um den Satz von Bedingungen anzugeben, den die Proxyfactory zum Erstellen des Proxys verwendet.

Wenn [**IUIAutomationProxyFactory::CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider)aufgerufen wird, übergibt Benutzeroberflächenautomatisierung Parameter, die das Proxyfactoryobjekt verwenden kann, um zu bestimmen, ob der Proxy das benutzerdefinierte Steuerelement angemessen unterstützt. Wenn dies der Fall ist, erstellt die Proxy factory eine Instanz des Proxys und gibt den [**IRawElementProviderSimple-Schnittstellenzeiger**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) zurück. Andernfalls wird ein **NULL-Zeiger** zurückgegeben.

## <a name="proxy-factory-mapping"></a>Proxy Factory-Zuordnung

Standardmäßig durchsucht Benutzeroberflächenautomatisierung die Proxy factory-Tabelle in der folgenden Reihenfolge.



| Auftrag | Proxy                        | BESCHREIBUNG                                                                      |
|-------|------------------------------|----------------------------------------------------------------------------------|
| 1     | Microsoft: Proxy ohne Steuerung | Für Fenster mit dem genauen Klassennamen oder Basisklassennamen "ComboBoxEx32".         |
| 2     | Microsoft: Proxy ohne Steuerung | Für Fenster mit dem genauen Klassennamen oder Basisklassennamen "WorkerW".              |
| 3     | Microsoft: Proxy ohne Steuerung | Für Fenster mit dem genauen Klassennamen oder Basisklassennamen "SHELLDLL \_ DefView".    |
| 4     | Microsoft: Containerproxy   | Für Fenster mit dem genauen Klassennamen oder Basisklassennamen \# "32770".              |
| 5     | Microsoft: Containerproxy   | Für Fenster mit einem Klassennamen oder Basisklassennamen, der "AfxControlBar" enthält.     |
| 6     | Microsoft: TreeView-Proxy    | Für Fenster mit einem Klassennamen oder Basisklassennamen, der "SysTreeView32" enthält.     |
| 7     | Microsoft: ListView-Proxy    | Für Fenster mit einem Klassennamen oder Basisklassennamen, der "SysListView32" (1) enthält. |
| 8     | Microsoft: ListView-Proxy    | Für Fenster mit einem Klassennamen oder Basisklassennamen, der "SysListView32" (2) enthält. |
| 9     | Microsoft: MSAA-Proxy        | Für ein beliebiges Fenster.                                                                  |



 

Proxys 7 und 8 sind doppelte Einträge für das SysListView32-Steuerelement. Ohne Änderung wird der Proxy 7 immer für das SysListView32-Steuerelement verwendet, und Proxy 8 wird nie verwendet. Proxy 8 wird nur für sichtbare Listenelemente verwendet und wird in der Regel von Clientanwendungen verwendet, die nur mit sichtbaren Elementen arbeiten oder strenge Leistungsanforderungen haben. Diese Clients können Proxy 7 entfernen.

Proxy 9, der Microsoft Active Accessibility Proxy Benutzeroberflächenautomatisierung, sollte immer der letzte Eintrag in der Tabelle sein. Dies ermöglicht Microsoft Active Accessibility Fallbackfunktionalität für Steuerelemente, die Microsoft Active Accessibility implementieren, aber nicht Benutzeroberflächenautomatisierung.

Beim Ändern von Einträgen in der Proxy factory-Tabelle sollten Sie die neue Position der Einträge sorgfältig auswerten. Es wird empfohlen, Einträge für benutzerdefinierte Proxys nach den Proxys ohne Steuerung und Container, aber vor dem Proxy Microsoft Active Accessibility Proxys Benutzeroberflächenautomatisierung werden. Auch wenn es möglich ist, dass Code im Aufruf von [**CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) bestimmt, ob er ein bestimmtes Fensterhand handle **(HWND)** unterstützen soll, ist es effizienter, Benutzeroberflächenautomatisierung den Proxy basierend auf dem Klassennamen auswählen zu lassen und den bedingten Code in der **CreateProvider-Methode** auf ein Minimum zu beschränken.

Benutzeroberflächenautomatisierung verwaltet eine separate Proxy factory-Tabelle für jeden Client. Wenn ein Client seine Proxytabelle ändert, wirken sich die Änderungen nur auf den Client selbst aus. andere Clients sind nicht betroffen.

## <a name="managing-default-proxies"></a>Verwalten von Standardproxies

Wenn eine Clientanwendung das [**CUIAutomation-Objekt**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) erstellt, enthält die Proxy factory-Tabelle anfänglich nur Einträge für die Standardproxyanbieter für Standardsteuerelemente. Mithilfe der [**IUIAutomationProxyFactoryMapping-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) können Clients neue Einträge hinzufügen, unerwünschte Einträge entfernen, die Reihenfolge der Einträge ändern und so weiter. Ein Client kann einen **IUIAutomationProxyFactoryMapping-Schnittstellenzeiger** abrufen, indem er die [**IUIAutomation::P rproxyFactoryMapping-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) aufruft.

Die Tabelle der verfügbaren Proxys enthält eine [**IUIAutomationProxyFactoryEntry-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) für jeden Proxy. Jede **IUIAutomationProxyFactoryEntry** gibt die [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) und die Steuerelementklasse an, die der Proxy verarbeitet, und definiert, wie Ereignisse behandelt werden sollen.

Die Tabelle der Proxys wird durch eine [**IUIAutomationProxyFactoryMapping-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) dargestellt, die aus der [**IUIAutomation::P rfaceFactoryMapping-Eigenschaft ermittelt werden**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) kann. Eine Anwendung kann **IUIAutomationProxyFactoryMapping-Methoden verwenden,** um Proxys hinzuzufügen und zu löschen. Um einen neuen Eintrag zu erstellen, der dieser Tabelle hinzugefügt werden soll, verwenden Sie [**IUIAutomation::CreateProxyFactoryEntry,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) um die Schnittstelle zu erhalten, und verwenden Sie dann die [**IUIAutomationProxyFactoryEntry-Methoden,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) um die anwendbare Steuerelementklasse und das Verhalten des Proxys zu definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Client-Side (Proxy) Benutzeroberflächenautomatisierung Anbieters](uiauto-howto-create-clientside-provider.md)
</dt> <dt>

[Benutzeroberflächenautomatisierung-Anbieterprogrammiererhandbuch](uiauto-providerportal.md)
</dt> </dl>

 

 