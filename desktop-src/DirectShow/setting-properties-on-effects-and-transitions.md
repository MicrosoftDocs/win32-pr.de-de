---
description: Festlegen von Eigenschaften für Effekte und Übergänge
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Festlegen von Eigenschaften für Effekte und Übergänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344155"
---
# <a name="setting-properties-on-effects-and-transitions"></a>Festlegen von Eigenschaften für Effekte und Übergänge

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Viele [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) haben Auswirkungen und Übergängen unterstützen Eigenschaften, die ihr Verhalten steuern. Eine Anwendung kann den Wert einer Eigenschaft mithilfe der [**ipropertysetter**](ipropertysetter.md) -Schnittstelle festlegen. Das zugrunde liegende Effekt-oder Übergangs Objekt muss **IDispatch** zum Festlegen der Eigenschaften unterstützen. Mit Video Effekten und-Übergängen kann die Anwendung einen Wertebereich festlegen, der sich im Laufe der Zeit ändert. (Sie können z. b. einen zurücksetzenübergang festlegen, um über den Frame hin und her zu wechseln.) Mit Audioeffekten ist der Wert der Eigenschaft statisch und kann sich im Laufe der Zeit nicht ändern. Die einzige Ausnahme ist der [volumeumschlags](volume-envelope-effect.md) Effekt, der eine dynamische Eigenschaft für die Volumeebene unterstützt.

Führen Sie die folgenden Schritte aus, um eine Eigenschaft festzulegen.

1.  Erstellen Sie eine Instanz des Eigenschaften Setters (CLSID \_ propertysetter).
2.  Füllen Sie die Struktur von [**Dexter \_ param**](dexter-param.md) -und [**Dexter- \_ Werten**](dexter-value.md) mit den Eigenschaften Daten aus. Diese Strukturen werden im folgenden erläutert.
3.  Übergeben Sie die " [**Dexter \_ param**](dexter-param.md) "-und " [**Dexter \_ value**](dexter-value.md) "-Strukturen an die [**ipropertysetter:: addprop**](ipropertysetter-addprop.md) -Methode.
4.  Wiederholen Sie die Schritte 2 und 3 für jede Eigenschaft, die Sie festlegen möchten.
5.  Übergeben Sie den [**ipropertysetter**](ipropertysetter.md) -Schnittstellen Zeiger an die [**iamtimelineobj:: setpropertysetter**](iamtimelineobj-setpropertysetter.md) -Methode.

Die " [**Dexter \_ param**](dexter-param.md) "-Struktur gibt an, welche Eigenschaft festgelegt wird. Sie enthält die folgenden Member.

-   **Name**: Name der Eigenschaft
-   **DISPID**: reserviert, muss NULL sein.
-   **nvalues**: Anzahl der Werte

Die \_ Wert Struktur von "Dexter" gibt den Wert einer Eigenschaft zu einem bestimmten Zeitpunkt an. Sie enthält die folgenden Member.

-   **v**: Variant-Typ, der einen neuen Wert für die-Eigenschaft angibt. Der **VT** -Member dieser Variante definiert den Datentyp der Eigenschaft. Weitere Informationen zum **Variant** -Typ finden Sie in der Windows SDK.
-   **RT**: Verweis Zeit, wenn die Eigenschaft diesen Wert annimmt, relativ zur Startzeit des Effekts oder Übergangs. Die Startzeit des Effekts oder Übergangs bezieht sich auf die Startzeit des übergeordneten Objekts.
-   **dwinterp**: Flag, das angibt, wie die-Eigenschaft vom vorherigen Wert in den neuen Wert geändert wird. Mit dem dexterf- \_ springflag springt die Eigenschaft zum angegebenen Zeitpunkt sofort in den neuen Wert. Beim dexterf- \_ interinterpolate-Flag wird die-Eigenschaft linear aus dem vorherigen Wert interpoliert.

Wenn Sie das **VT** -Element auf VT \_ BSTR festlegen, führt der Eigenschaften Setter alle notwendigen Konvertierungen aus. Fügen Sie für Gleit Komma Werte die führende Null vor der Dezimalstelle ein. Beispielsweise 0,3, nicht. 3.

> [!Note]  
> Anwendungen sollten die Konvertierung von **BSTR**-s in numerische Werte vermeiden. Wenn die Eigenschaft einen numerischen Wert aufweist, verwenden Sie den entsprechenden numerischen **Variant** -Typ.

 

Der Wert einer Eigenschaft kann sich im Laufe der Zeit ändern, sodass die [**ipropertysetter:: addprop**](ipropertysetter-addprop.md) -Methode eine einzelne " [**Dexter \_ param**](dexter-param.md) "-Struktur und einen Zeiger auf ein Array von " [**Dexter \_ value**](dexter-value.md) "-Strukturen annimmt. Das Array definiert einen Satz zeitbasierter Werte für die-Eigenschaft. Die Elemente des Arrays müssen sich in aufsteigender Zeitreihen Folge befinden, und der **nvalues** -Member der "Dexter \_ Param"-Struktur muss der Länge des Arrays entsprechen.

Im folgenden Codebeispiel werden Eigenschafts Daten für den [SMPTE](smpte-wipe-transition.md) -Umleitungs Übergang erstellt. Der Code wird auf 120 festgelegt, wodurch ein Oval-zurücksetzen erstellt wird. Die Verweis Zeit wird auf NULL festgelegt, was den Beginn des Übergangs angibt.


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



**Dynamisch veränderliche Eigenschaften**

Nachdem Sie ein Video Bearbeitungs Projekt gerenkt haben, ist es möglich, die Eigenschaften eines Effekts oder Übergangs Objekts während der Ausführung des Diagramms zu ändern. Dies ist jedoch nur möglich, wenn Sie Eigenschaften für dieses Objekt festlegen, bevor die Anwendung den Namen " [**unenderengine:: connectfrontend**](irenderengine-connectfrontend.md)" hat. Wenn dies der Fall ist, können Sie [**iamtimelineobj:: getpropertysetter**](iamtimelineobj-getpropertysetter.md) für den Effekt oder Übergang aufrufen, die Eigenschaften löschen oder ändern, und die Änderungen werden dynamisch durchgeführt, wenn das Diagramm ausgeführt wird. Während der Änderung können visuelle Anomalien auftreten, daher wird dies nur für die Vorschau empfohlen. Ändern Sie die Eigenschaften nicht, während Sie das Projekt in eine Datei schreiben.

Wenn Sie keine Eigenschaften für den Effekt oder das Übergangs Objekt festgelegt haben, bevor Sie **connectfrontend** aufgerufen haben, können Sie ihm während der Ausführung des Diagramms keine Eigenschaften hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



