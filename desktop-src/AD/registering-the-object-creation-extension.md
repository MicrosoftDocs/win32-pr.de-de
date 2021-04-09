---
title: Die Objekt Erstellungs Erweiterung wird registriert.
description: Wenn eine Erweiterungs-DLL für die Objekt Erstellung in Active Directory Domain Services erstellt wird, muss Sie in der Windows-Registrierung registriert und Active Directory Domain Services werden, damit com und die Active Directory Verwaltungs-MMC-Snap-Ins die Erweiterung berücksichtigen.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948550"
---
# <a name="registering-the-object-creation-extension"></a>Die Objekt Erstellungs Erweiterung wird registriert.

Wenn eine Erweiterungs-DLL für die Objekt Erstellung in Active Directory Domain Services erstellt wird, muss Sie in der Windows-Registrierung registriert und Active Directory Domain Services werden, damit com und die Active Directory Verwaltungs-MMC-Snap-Ins die Erweiterung berücksichtigen.

## <a name="registering-in-the-windows-registry"></a>Registrieren in der Windows-Registrierung

Wie alle com-Server muss eine Erweiterung zum Erstellen von Objekten in der Windows-Registrierung registriert werden. Die Erweiterung ist unter folgendem Schlüssel registriert:

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

" &lt; Extension CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird. " &lt; Erweiterungs Pfad &gt; " enthält den Pfad und den Dateinamen der Erweiterungs-DLL. Der **ThreadingModel** -Wert für alle Objekt Erstellungs Erweiterungen muss "Apartment" lauten.

## <a name="registering-with-active-directory-domain-services"></a>Registrieren bei Active Directory Domain Services

Die Registrierung der Objekt Erstellungs Erweiterung ist spezifisch für ein Gebiets Schema. Wenn die Objekt Erstellungs Erweiterung auf alle Gebiets Schemas angewendet wird, muss Sie im **Display specifier** -Objekt der Objektklasse in allen Gebiets Schema-subcontainern im DisplaySpecifiers-Container registriert werden. Wenn die Objekt Erstellungs Erweiterung für ein bestimmtes Gebiets Schema lokalisiert wird, registrieren Sie Sie im **displaySpecifier** -Objekt im unter Container dieses Gebiets Schemas. Weitere Informationen über den displayspecifieres-Container und die Gebiets Schemas finden Sie unter [anzeigen](display-specifiers.md) von Bezeichner und [displaySpecifier-Containern](displayspecifiers-container.md).

Es gibt zwei displaySpecifier-Attribute, unter denen eine Objekt Erstellungs Erweiterung registriert werden kann. Hierbei handelt es sich um den Ordner " **kreationwizard** **" und "**".

Das Attribut " **kreationwizard** " identifiziert Erweiterungen der primären Objekt Erstellung, um den vorhandenen Assistenten oder den Assistenten zum Erstellen von systemeigenen Objekten in Active Directory administrativen Snap-Ins zu ersetzen Eine primäre Erstellungs Erweiterung stellt die erste Gruppe von Seiten bereit und wird auf die gleiche Weise wie Native Seiten gehostet. Dieses Attribut ist einwertig und erfordert das folgende Format:


```C++
<CLSID>
```



Die " &lt; CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID des COM-Objekts, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.

Das Attribut " **kreatewizardecoxt** " identifiziert Erweiterungen für die Erstellung sekundärer Objekte. Eine sekundäre Erstellungs Erweiterung fügt der systemeigenen Seite oder der primären Erweiterung Assistenten Seiten hinzu. Dieses Attribut ist mehr wertig und erfordert folgendes Format:


```C++
<order number>,<CLSID>
```



" &lt; Order Number &gt; " ist eine nicht signierte Zahl, die die Position der Seite im Assistenten darstellt. Wenn ein Erstellungs-Assistent angezeigt wird, werden die Werte anhand eines Vergleichs der "Order Number"-Werte der einzelnen Werte sortiert &lt; &gt; . Wenn mehr als ein Wert dieselbe " &lt; Bestellnummer" aufweist &gt; , werden diese Seiten in der Reihenfolge geladen, in der Sie vom Active Directory Server gelesen werden. Wenn möglich, sollten Sie eine nicht vorhandene " &lt; Bestellnummer" verwenden &gt; (d. h. eine, die nicht von anderen Werten in der-Eigenschaft verwendet wurde). Es gibt keine vorgeschriebene Anfangsposition, und Lücken sind in der Sequenz " &lt; Order Number &gt; " zulässig.

Die " &lt; CLSID &gt; " ist die Zeichen folgen Darstellung der CLSID des COM-Objekts, die von der [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) -Funktion erstellt wird.

 

 