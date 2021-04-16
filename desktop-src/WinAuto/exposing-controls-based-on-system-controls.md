---
title: Verfügbar machen von Steuerelementen basierend auf System Steuerelementen
description: Verfügbar machen von Steuerelementen basierend auf System Steuerelementen
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390779"
---
# <a name="exposing-controls-based-on-system-controls"></a>Verfügbar machen von Steuerelementen basierend auf System Steuerelementen

Sie sollten die Verwendung einer Form dynamischer Anmerkung – Direct, Value Map oder Server – in Erwägung gezogen, bevor Sie das in diesem Abschnitt beschriebene Verfahren ausführen. Weitere Informationen finden Sie unter [Dynamic Annotation-API](dynamic-annotation-api.md).

In den meisten Fällen stellt Microsoft Active Accessibility Informationen zu übergeordneten oder untergeordneten Steuerelementen bereit. Mithilfe von übergeordneten Klassen und Unterklassen können Anwendungsentwickler ein benutzerdefiniertes Steuerelement mit den grundlegenden Funktionen eines System Steuer Elements erstellen und Erweiterungen einschließen, die von der Anwendung bereitgestellt werden. Ein übergeordnetes Steuerelement hat einen anderen Fenster Klassennamen als das System Steuerelement, auf dem es basiert. Ein Unterklassen-Steuerelement hat denselben Fenster Klassennamen. Weitere Informationen zu übergeordneten Klassen und Unterklassen finden Sie in der Dokumentation zum Windows Software Development Kit (SDK).

Da Microsoft Active Accessibility Informationen zu vom System bereitgestellten Steuerelementen verfügbar macht, macht Microsoft Active Accessibility das geänderte Steuerelement verfügbar, es sei denn, ein übergeordnetes oder untergeordnetes Steuerelement unterscheidet sich deutlich vom Basis Steuerelement. Um zu ermitteln, ob auf das geänderte Steuerelement zugegriffen werden kann, sollten Anwendungsentwickler Dienstprogramme wie z. b. über [prüfen](inspect-objects.md) und [barrierefreie Ereignis](accessible-event-watcher.md) Überwachung verwenden, um das Verhalten des geänderten Steuer Elements mit dem Basis Steuerelement zu vergleichen

Wenn Sie nach der Verwendung dieser Hilfsprogramme feststellen, dass auf das geänderte Steuerelement nicht zugegriffen werden kann, müssen Sie das Steuerelement wie jedes andere benutzerdefinierte Steuerelement behandeln. Das Steuerelement muss Ereignisse auslöst, und die Fenster Prozedur der Anwendung muss auf die [**WM- \_ GetObject**](wm-getobject.md)-Nachricht reagieren, indem eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle bereitgestellt wird, die Client Anwendungen zum Abrufen von Informationen über das Steuerelement verwenden.

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a>"Kreatestdaccessibleproxy" und "kreatestdaccessibleobject"

Wenn alle oder die meisten der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften für das geänderte Steuerelement mit dem Basis Steuerelement identisch sind [**, verwenden Sie**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) "" [**, um die**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) Implementierung der **IAccessible** -Schnittstelle des Steuer Elements zu vereinfachen.

> [!Note]  
> Beachten Sie beim überlagern oder Unterklassen für ein barrierefreies Steuerelement, dass das Objekt, das von der Funktion "Funktion" von "| [**atestdaccessibleobject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) " abgerufen wurde, möglicherweise mehr als nur die Schnittstelle [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementiert Sie kann andere Schnittstellen wie [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)enthalten. Möglicherweise müssen Sie diese zusätzlichen Schnittstellen umschließen, um die von der ursprünglichen Implementierung des Steuer Elements bereitgestellte Barrierefreiheits Unterstützung beizubehalten.

 

Die Funktionen " [**foratestdaccessibleproxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) " und " [**foratestdaccessibleobject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) " rufen einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger für das angegebene System Steuerelement ab. Der Unterschied in diesen Funktionen besteht darin, dass von " **kreatestdaccessibleobject** " der Fenster Klassenname verwendet wird, der aus seinem *HWND* -Parameter abgerufen wird, während " **kreatestdaccessibleproxy** " den Fenster Klassennamen verwendet, der in seinem *szclassname* Wenn Sie sich entscheiden, diese Funktionen zu verwenden, verwenden Sie daher " **foratestdaccessibleproxy** ", um Informationen über übergeordnete Steuerelemente verfügbar zu machen, und jede Funktion mit untergeordneten Steuerelementen.

Nachdem Sie einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger auf das System Steuerelement erhalten haben, verwenden Sie den-Zeiger in der Implementierung der **IAccessible** -Schnittstelle für das geänderte-Steuerelement. Wenn eine Eigenschaft oder Methode für das geänderte Steuerelement mit dem Basis Steuerelement identisch ist, verwenden Sie den **IAccessible** -Zeiger, um die vom Basis Steuerelement bereitgestellten Informationen zurückzugeben. Wenn sich eine Eigenschaft für das geänderte Steuerelement vom Basis Steuerelement unterscheidet, überschreiben Sie die-Eigenschaft des Basis Steuer Elements.

Im folgenden Beispiel ist **cacccustombutton** die Anwendungs definierte Klasse, die von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)abgeleitet ist. Die Member-Variable **m \_ paccdefaultbutton** ist ein Zeiger auf eine **IAccessible** -Schnittstelle, die während der Initialisierungs Prozedur für das-Steuerelement von " [**foratestdaccessibleobject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) " abgerufen wurde. In diesem Beispiel ist die **Role** -Eigenschaft für das benutzerdefinierte Steuerelement identisch mit der **Role** -Eigenschaft des System Steuer Elements, sodass die **Role** -Eigenschaft des Basis Steuer Elements zurückgegeben wird. Allerdings unterscheidet sich die **Description** -Eigenschaft von der des Basis Steuer Elements, sodass diese Eigenschaft überschrieben wird.


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



Weitere Informationen zu den Eigenschaften und Methoden von System Steuerelementen in [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) finden Sie [unter Anhang A: Unterstützte Elemente der Benutzeroberflächen Elemente](appendix-a--supported-user-interface-elements-reference.md).

 

 