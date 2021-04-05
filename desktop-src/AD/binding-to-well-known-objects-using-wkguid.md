---
title: Binden an Well-Known Objekte mithilfe von wkguid
description: In diesem Thema wird gezeigt, wie mithilfe der wkguid-Bindungs Zeichenfolge an Objekte gebunden wird.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Binden an Well-Known Objekte mithilfe von wkguid AD
- Active Directory mithilfe von, Bindung und Verwendung von wkguid für die Bindung an bekannte Objekte
- bekannte Objekte (AD)
- bekannte Objekte (AD), binden an mithilfe von wkguid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724648"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a>Binden an Well-Known Objekte mithilfe von wkguid

Container können über ein oder mehrere wichtige unter Objekte verfügen, die umbenannt oder verschoben werden können. Es kann schwierig sein, diese unter Objekte zu verfolgen und richtige Bindungs Zeichenfolgen zu erstellen, insbesondere, wenn Sie umbenannt oder verschoben werden.

Um die Umbenennungs sichere Bindung an diese Objekte innerhalb dieser Container zu unterstützen, Active Directory Domain Services über zwei Attribute verfügen: **wellKnownObjects** und **otherWellKnownObjects**. Diese Attribute verfügen über eine Attribut Syntax von adstype \_ DN \_ with \_ Binary. Sie lassen mehrere Werte zu und enthalten die GUID/DN-Tupel bekannter Objekte in den Containern, für die Sie festgelegt sind. Der Active Directory Server verwaltet den Distinguished Name-Teil jedes **wellKnownObjects** -und **otherWellKnownObjects** -Eintrags, sodass er den aktuellen Distinguished Name des Objekts enthält, das beim Erstellen des Eintrags angegeben wurde.

Die **otherWellKnownObjects** -Eigenschaft kann für jedes beliebige Objekt festgelegt und verwendet werden.

Die **wellKnownObjects** -Eigenschaft wird für die Domänen DNS-und Konfigurations Container verwendet. Die **wellKnownObjects** -Eigenschaft ist eine reine System Eigenschaft und kann nur vom Betriebssystem geändert werden.

Der **domainDns** -Container verfügt über die folgenden bekannten Objekte:

-   Benutzer
-   Computer
-   System
-   Domänencontroller
-   Infrastruktur
-   Gelöschte Objekte
-   Verloren und gefunden

Der Konfigurations Container verfügt über das bekannte Objekt: Gelöschte Objekte.

Diese Objekte befinden sich in jedem **Domänen DNS** -und Konfigurations Container in einem Active Directory-Domäne-Dienst.

Sie können eine Bindung an ein bekanntes Objekt mithilfe des wkguid-Bindungs Formats herstellen. Die Bindung mit wkguid wird nur in Active Directory Domain Services unterstützt, d. h. im LDAP-Anbieter.

> [!IMPORTANT]
> Verwenden Sie immer das Bindungs Format wkguid, um eine Bindung an die bekannten Objekte (wie oben) in den Domänen-und Konfigurations Containern herzustellen. Dadurch wird sichergestellt, dass diese Container auch dann an gebunden werden können, wenn Sie verschoben oder umbenannt werden.

 

Das Format der wkguid-Bindungs Zeichenfolge lautet wie folgt:


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



" &lt; Servername &gt; " ist der Name des Verzeichnis Servers. Der " &lt; Servername &gt; " ist optional.

" &lt; XXXXX &gt; " ist die Zeichen folgen Darstellung des hexadezimal Werts der GUID, die das bekannte Objekt darstellt. Die GUID-Zeichenfolge wird im Formular "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" angegeben und ist nicht identisch mit der GUID-Zeichenfolge, die von der [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) -Funktion erstellt wird, die das Format "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" annimmt. Weitere Informationen und ein Codebeispiel, das zeigt, wie eine bindbare Zeichenfolge aus einer GUID erstellt wird, finden Sie unter [Beispielcode zum Erstellen einer typfähigen Zeichen folgen Darstellung einer GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).

Um an ein Objekt zu binden, das in **otherWellKnownObjects** in einem Objekt angegeben ist, geben Sie " &lt; XXXXX &gt; " als Bindungs Zeichenfolgen-Form der bekannten Objekt-GUID des Objekts an. Weitere Informationen finden Sie unter [Lesen der objectGUID eines Objekts und Erstellen einer Zeichen folgen Darstellung der GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md). Weitere Informationen zum Festlegen der **otherWellKnownObjects** -Eigenschaft für Objekte finden Sie unter [Aktivieren der Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).

Geben Sie zum Binden an ein in **wellKnownObjects** in domainDNS oder in Konfigurations Containern angegebenes Objekt " &lt; XXXXX &gt; " als eine der folgenden Konstanten an, die in der folgenden Tabelle aufgeführt sind, wie in "NTDSAPI. h" definiert.



| Container          | GUID-Bezeichner                         |
|--------------------|-----------------------------------------|
| Benutzer              | GUID- \_ Benutzer \_ Container \_ W               |
| Computer          | GUID- \_ computrs- \_ Container \_ W            |
| System             | GUID- \_ Systeme \_ Container \_ W             |
| Domänencontroller | GUID- \_ Domänen \_ Controller \_ Container \_ W |
| Infrastruktur     | GUID- \_ Infrastruktur \_ Container \_ W      |
| Gelöschte Objekte    | GUID- \_ Gelöschte \_ Objekte \_ Container \_ W    |
| Verloren und gefunden     | GUID \_ LostAndFound- \_ Container \_ W        |



 

Wenn Sie z. b. eine Bindung an den Benutzer Container in einer Domäne herstellen möchten, geben Sie den **GUID- \_ Benutzer \_ Container \_ W** als " &lt; XXXXX &gt; " an.

" &lt; Container DN &gt; " ist der Distinguished Name des Container Objekts, für das dieses Objekt in seiner **wellKnownObjects** -Eigenschaft als Wert dargestellt wird. Wenn Sie z. b. eine Bindung an den Benutzer Container in einer Domäne herstellen möchten, geben Sie den Distinguished Name der Domäne als " &lt; Container-DN &gt; " an.

Um z. b. an den Benutzer Container der Domäne fabrikam.com zu binden, verwenden Sie die folgende Bindungs Zeichenfolge.

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie eine Bindung an eine bekannte GUID finden, finden Sie unter [Beispielcode für die Bindung an bekannte Objekte](example-code-for-binding-to-well-known-objects.md).

 

 