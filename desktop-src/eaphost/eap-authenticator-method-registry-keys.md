---
title: Registrierungs Werte der EAP-Authenticator-Methode
description: Weitere Informationen zu den Registrierungs Werten der EAP Authenticator-Methode. Diese spezifischen Registrierungs Werte sind für EAP Authenticator-Methoden erforderlich.
ms.assetid: 9374f9f7-b088-4e3a-ac96-8ccbeda87bb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a710ca6f09914c8d111c42a8323a9c39c51f898
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949127"
---
# <a name="eap-authenticator-method-registry-values"></a>Registrierungs Werte der EAP-Authenticator-Methode

Bestimmte Registrierungs Werte sind für EAP Authenticator-Methoden erforderlich.

## <a name="eap-authenticator-method-dll-paths"></a>DLL-Pfade der EAP-Authenticator-Methode

Der folgende Pfad gibt den Registrierungs Speicherort für reguläre EAP Authenticator-Methoden-DLLs an.

**HKLM \\ System \\ CCS \\ \\ -Dienste EAPHost- \\ Methoden \\ *&lt; AutorID &gt;* \\ * &lt; eaptypeid&gt;***

Beispielsweise wird ein Installationspfad der EAP Authenticator-Methode, der eine **AutorID** von "311" (gibt an, dass "Microsoft" der Autor ist) und die **eaptypeid** "40" angezeigt, wie folgt angezeigt.

**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ 311 \\ 40**

Der folgende Pfad gibt den Registrierungs Speicherort für erweiterte EAP Authenticator-Methoden-DLLs an.

**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ *&lt; AutorID &gt;* \\ 254 \\ *&lt; VendorID &gt;* \\ * &lt; vendortype&gt;***

Beispielsweise wird ein Installationspfad der EAP Authenticator-Methode für die **Autorisierung mit der Autorisierung** "311" (die besagt, dass "Microsoft" der Autor ist), der **VendorID** "311" und der **eaptypeid** "40" wie folgt angezeigt.

**HKLM \\ System \\ CCS- \\ Dienste \\ EAPHost- \\ Methoden \\ 311 \\ 254 \\ 311 \\ 40**

> [!Note]  
> Weitere Informationen zur Zuordnung von EAP-Methoden Typen finden Sie im Abschnitt 6,2 von [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016).

 

## <a name="registry-values"></a>Registrierungs Werte

Die folgenden Registrierungs Werte für die Authenticator-Methode sind erforderlich.

-   [Authentierordllpath](#authenticatordllpath)
-   [Authenti-FriendlyName](#authenticatorfriendlyname)

Neben den oben aufgeführten Registrierungs Werten wird der folgende Authentifikator-Methoden Registrierungs Wert empfohlen.

-   [Eigenschaften](#properties)

Die verbleibenden Registrierungs Werte der Authenticator-Methode sind optional.

-   [Configclsid](#configclsid)
-   [Standalonesupportiert](#standalonesupported)

## <a name="authenticatordllpath"></a>Authentierordllpath



| Konstanter Wert | Authentierordllpath                                                                                          |
|----------------|---------------------------------------------------------------------------------------------------------------|
| type           | REG \_ Expand \_ SZ                                                                                               |
| BESCHREIBUNG    | Der Pfad zur EAP Authenticator-Methoden-dll. Beispiel:% systemroot% \\ system32 \\ &lt; Name \_ von \_ dll &gt; . dll. |



 

## <a name="authenticatorfriendlyname"></a>Authenti-FriendlyName



| Konstanter Wert | Authenti-FriendlyName                                                          |
|----------------|------------------------------------------------------------------------------------|
| type           | REG- \_ SZ                                                                            |
| BESCHREIBUNG    | Eine Zeichenfolge, die den anzeigen Amen für die EAP-Authenticator-Methode enthält. |



 

## <a name="configclsid"></a>Configclsid



| Konstanter Wert | Configclsid                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG- \_ SZ                                                                                                                               |
| BESCHREIBUNG    | Zeichenfolge, die die Konfigurations Klassen-GUID für diese Authenticator-Methode im Format {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} enthält. |



 

## <a name="properties"></a>Eigenschaften



| Konstanter Wert | Eigenschaften                                                                                                                                                  |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type           | REG \_ DWORD                                                                                                                                                  |
| BESCHREIBUNG    | Bits in DWORD sind so festgelegt, dass die Unterstützung für die Eigenschaft angegeben wird. Eine Liste der unterstützten Werte finden Sie unter [**Eigenschaften der EAP-Methode**](eap-method-properties.md). |



 

## <a name="standalonesupported"></a>Standalonesupportiert



| Konstanter Wert | Standalonesupportiert                                             |
|----------------|-----------------------------------------------------------------|
| type           | REG \_ DWORD                                                      |
| BESCHREIBUNG    | 0, wenn es sich um eine eigenständige Authenticator-Methode handelt. 1, wenn dies nicht der Fall ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungsschlüssel für die EAP-Peer Methode](eap-peer-method-registry-keys.md)
</dt> <dt>

[Registrierungs Konfiguration für erweiterte EAP-Typen](registry-keys-for-eap-methods.md)
</dt> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> <dt>

[RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)
</dt> </dl>

 

 




