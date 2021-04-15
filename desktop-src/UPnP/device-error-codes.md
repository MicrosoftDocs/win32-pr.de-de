---
title: Gerätefehler Codes
description: Die InvokeAction-und QueryStatus-ariable-Methoden geben HRESULT-Werte zurück, die möglicherweise auf einen Gerätefehler hinweisen (d. h. einen Fehler, der von einem UPnP-zertifizierten Gerät empfangen wird).
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474541"
---
# <a name="device-error-codes"></a>Gerätefehler Codes

Die [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) -und [**QueryStatus-ariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) -Methoden geben **HRESULT** -Werte zurück, die möglicherweise auf einen Gerätefehler hinweisen (d. h. einen Fehler, der von einem UPnP-zertifizierten Gerät empfangen wird). Wenn ein Fehler von einem Gerät empfangen wird, gibt die Methode ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) oder [**QueryStatus**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) einen **HRESULT** -Wert zurück, der auf dem Gerätefehler Code basiert, wie in diesem Thema erläutert. Da eine Konvertierung auf den Gerätefehler Code angewendet wird, um einen **HRESULT** -Wert zu erhalten, können Sie den Fehlercode des Geräts nicht direkt aus dem **HRESULT** -Wert lesen.

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a>Konvertierung eines Gerätefehler Codes in ein HRESULT

Es gibt sowohl standardmäßige als auch nicht standardmäßige Gerätefehler Codes. Die Standard Codes haben in allen UPnP-zertifizierten Geräten dieselbe Bedeutung und verfügen über Werte, die kleiner als 600 sind. Die nicht standardmäßigen Codes sind Hersteller spezifisch und weisen Werte zwischen 600 und 899 auf.

Unabhängig davon, ob der Gerätefehler Code "Standard" ist, bestimmt, wie der **HRESULT** -Wert generiert wird:

-   Ein standardmäßiger Gerätefehler Code ist einem **HRESULT** -Wert zugeordnet.

<!-- -->

-   Ein nicht standardmäßiger Gerätefehler Code wird durch Anwenden einer Formel in den **HRESULT** -Wert eingebettet.

Beide Verfahren können umgekehrt werden, um den Gerätefehler Code aus einem bestimmten **HRESULT** -Wert zu bestimmen.

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a>Ableiten eines Gerätefehler Codes von einem HRESULT-Wert

Wenn der **HRESULT** -Wert größer als oder gleich **UPnP \_ e \_ Action \_ Specific \_ Base** (0x80040300) und kleiner als oder gleich **UPnP \_ e \_ Action \_ Specific \_ Max** (0x8004042b) ist, ist der Fehlercode des Geräts nicht dem Standard – verwenden Sie die Formel im folgenden Abschnitt, um den Fehlercode zu ermitteln. Andernfalls ist der Gerätefehler Code Standard – verwenden Sie die Tabelle im Abschnitt Mapping for Standard Device Error Codes, die die Zuordnung vom **HRESULT** -Wert zum Gerätefehler Code bereitstellt.

Legen Sie für eine Textbeschreibung des Fehlers nach einem Aufruf von [**iupnpservice:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction)den *pvarretval* -Parameter auf ein leeres Array fest. Bei der Rückgabe enthält dieser Parameter eine Textbeschreibung des Fehlers, sofern aufgetreten.

### <a name="formula-for-nonstandard-device-error-codes"></a>Formel für nicht dem Standard entsprechende Gerätefehler Codes

Verwenden Sie die folgende Formel, wenn **UPnP \_ e \_ Action Specific \_ \_ Base** für **HRESULT** -**UPnP \_ e \_ Action \_ Specific \_ Max**.

Gerätefehler Code = (**HRESULT**  -  **UPnP \_ E \_ Action \_ Specific \_ Base**) + **Fehler \_ Aktions \_ spezifische \_ Basis**

Durch Ersetzen der tatsächlichen numerischen Werte ist die Gleichung: Gerätefehler Code = (**HRESULT** -0x80040300) + 0x0258

### <a name="mapping-for-standard-device-error-codes"></a>Zuordnung für Standard Geräte-Fehler Codes

Verwenden Sie die folgende Zuordnung, wenn **HRESULT**  <  **UPnP \_ E \_ Action \_ Specific \_ Base** ist.



| HRESULT-Wert                    | Gerätefehler Code                | Tatsächlicher Wert |
|----------------------------------|----------------------------------|--------------|
| UPnP \_ E \_ ungültige \_ Aktion.         | \_ungültige \_ Aktion           | 401          |
| UPnP \_ E \_ ungültige \_ Argumente.      | Fehler \_ ungültiges \_ arg              | 402          |
| UPnP \_ E \_ nicht \_ \_ synchron           | \_ungültige \_ Sequenz \_ Nummer | 403          |
| UPnP \_ E \_ ungültige \_ Variable.       | \_ungültige \_ Variable.         | 404          |
| UPnP \_ E- \_ Aktions \_ Anforderung \_ fehlgeschlagen | \_ \_ interner \_ Fehler des Fehler Geräts   | 501          |



 

## <a name="more-information"></a>Weitere Informationen

Gerätefehler Codes werden in der [UPnP-Geräte Architektur Version 1,0](https://openconnectivity.org/resources/documents.asp)angegeben. Die in diesem Thema erwähnten Konstanten sind in den Dateien "UPnP. h" und "UPnP. idl" definiert.

 

 




