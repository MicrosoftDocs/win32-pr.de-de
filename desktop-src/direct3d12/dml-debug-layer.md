---
title: Verwenden der directml-debugschicht
description: Die directml-debugschicht ist eine optionale Entwicklungszeit Komponente, die Sie beim Debuggen Ihres directml-Codes unterstützt.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548685"
---
# <a name="using-the-directml-debug-layer"></a>Verwenden der directml-debugschicht

Die directml-debugschicht ist eine optionale Entwicklungszeit Komponente, die Sie beim Debuggen Ihres directml-Codes unterstützt. Die Debug-Ebene ist Teil eines separaten Grafik Toolpakets, das als [Feature-on-Demand](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD) verteilt wird. Die Grafik Tools-FOD muss auf dem System installiert sein, damit die Debugebene verwendet werden soll.

Es wird dringend empfohlen, dass Sie die debugschicht bei der Entwicklung von Anwendungen mithilfe von directml aktivieren, da Sie im Falle einer ungültigen API-Verwendung wertvolle Informationen bereitstellen kann.

## <a name="installing-the-directml-debug-layer"></a>Installieren der directml-debugschicht

Um das optionale FOD-Paket (Feature-on-Demand) für Grafik Tools zu installieren, führen Sie den folgenden Befehl an einer PowerShell-Eingabeaufforderung aus.

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

Alternativ können Sie das Grafik Toolpaket in den Windows 10-Einstellungen installieren. Navigieren Sie zu **Einstellungen**  >  **apps** apps  >  **& Features**  >  **optionale Features Features**  >  **Hinzufügen** > und wählen Sie dann **Grafik Tools** aus.

## <a name="enabling-the-directml-debug-layer"></a>Aktivieren der directml-debugschicht

Sobald das Grafik Tools-Paket installiert ist, können Sie die directml-debugschicht durch Bereitstellen von  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) aktivieren, wenn Sie [**dmlkreatedevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice)aufrufen.

> [!IMPORTANT]
> Sie müssen zuerst die debugschicht Direct3D 12 aktivieren. Aktivieren Sie *anschließend* die directml-debugschicht durch Aufrufen von **dmlcreatedevice**.

Nachdem Sie die directml-Debugebene aktiviert haben, führen alle directml-Fehler oder ungültigen API-Aufrufe dazu, dass Debuginformationen als Debugausgabe ausgegeben werden. Hier sehen Sie ein Beispiel.

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a>Siehe auch

* [Dmlkreatedevice-Funktion](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [Verfügbare Features: Bedarfs gesteuert](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [Verwenden der GPU-basierten Validierung mit der Direct3D 12-Debugebene](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [Direct3D 12-Debug-Ebenenverweis](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
